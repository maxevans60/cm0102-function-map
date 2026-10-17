# CM 01/02 function map

A map of every function in `cm0102.exe` 3.9.68, the last official patch of Championship Manager 01/02. Each of the 6,863 game and library functions has its address, the source file it came from, a name, its calling convention and one sentence on what it does.

The data map covers the 4,428 global variables that these functions touch. Each global has its address, size, type, a name, one sentence on what it holds, and the functions that read and write it.

Search both by address (the offset that Olly shows) or by word: **https://maxevans60.github.io/cm0102-function-map/**

The map came out of the [Bosman Edition](https://github.com/maxevans60/cm0102-bosman-edition), a recompiled port of the game to Mac, Windows and Linux. It is free for anyone who patches, mods or studies the game.

## Look up an offset or address

The map uses the addresses that OllyDbg and x64dbg show, written as `0x8e7810`. Olly shows the same address as `008E7810`. On the champman0102 forum these are called offsets.

- Some offsets in patch lists are positions in the exe file. Add 0x400000 to one, or tick "File offset" on the search page.
- Most patch offsets lie inside a function. The search page shows the function that holds the address.
- An address in the data section, such as `0xae2c90`, gives the global at that address, or the global that holds it.
- The search also takes a word, such as `loan`, `prize`, `League::` or `g_current_date`.
- Each result links on. A function lists the globals it uses, and a global lists the functions that read and write it.

## Files

| File | What it holds |
|---|---|
| [`map/index.md`](map/index.md) | Every source file with its number of functions |
| `map/<file>.cpp.md` | One page for each source file: address, size, name, convention, purpose, confidence |
| [`map/functions.tsv`](map/functions.tsv) | All named functions with every column, for scripts and spreadsheets |
| [`map/names.tsv`](map/names.tsv) | Address, file, name, confidence, model and the research docs that cite it |
| [`map/not-high.tsv`](map/not-high.tsv) | Every row that is not high, with one line on what is missing for high |
| [`map/function-files.tsv`](map/function-files.tsv) | All 11,747 function starts, unwind funclets and runtime code included, with their file |
| [`data-map/index.md`](data-map/index.md) | Every owner file with its number of globals |
| `data-map/<file>.cpp.md` | The globals of one owner file: address, size, type, name, description, evidence, confidence, writers, readers |
| [`data-map/shared.md`](data-map/shared.md) | The 463 globals that four or more files use with no main owner, such as the current date and the read-only constants |
| [`data-map/globals.tsv`](data-map/globals.tsv) | All 4,428 globals with address, size, type, name, readers, writers and confidence |
| [`data-map/data.tsv`](data-map/data.tsv) | All globals with their owner file and description, for the search page and for scripts |

The source file names come from the assert strings in the exe, such as `E:\dev\CM3\cm3 00-01\cm3\code\comp\leagues\league.cpp`. A function without an assert of its own gets the file of the code around it. A competition class keeps the method names of its base class for each vtable slot, so `SweCup::update_staff_records_for_status` is slot 17 of the cup vtable.

## How the map was made

AI agents (Claude Opus, and Sonnet for 254 library functions) read each function. They read its strings, asserts, callers, callees, vtable slots and decompiled code, and gave it a name. Then fresh agents reviewed every name with medium or low confidence, every shared stub and every false entry. A third agent settled each disagreement. The review changed 842 names. A confidence pass then gave the agents the names of the globals and of the reviewed neighbours, and checked the medium and low rows again. It raised 245 rows to high and changed 10 names.

Each row has a confidence:

- **high** (5,702): the evidence quotes a string, a caller or a vtable slot that pins the purpose.
- **medium** (1,133): the shape of the code and the callers agree, but no single fact proves the name.
- **low** (28): a guess.

Read the code before you build a patch on a medium or low name. A name helps you find code. It does not prove what the code does.

The data map lists each global on the page of its owner file: the file of most of the functions that use it. A script named 3,015 globals from facts in the exe: the key ids, the read-only constants by value, the vtables by their constructor, and the string pointers. Agents (Claude Sonnet, and Opus for one) named the other 1,413 from the functions that read and write them, then a confidence pass checked them again. The description of a field of an object reads `g_<object>+0x<offset> <field>`. Of the 4,428 globals, 3,808 are high, 574 medium and 46 low.

Every name comes from reading the exe's own code. While they worked, the agents also had the Offset Index thread on the champman0102 forum to hand as a check. Where the thread names a global or a field, they compared it with the code before they used it. Rows that rest on it say "forum offset index" in their evidence. Thanks to everyone who added to that thread.

## What the map holds

The map holds names, file names and short descriptions. It holds no code, decompiled code or data of the original game. To read the code you need your own copy of the game. Eidos made it free in 2008.

## Report a wrong name

Open an issue with the address, the name you think is right and what the code does. A caller, a string or a field offset helps most. The map is generated from the Bosman Edition repo, so a pull request that edits `map/` or `data-map/` would be overwritten. The fix goes into the next update of the map.

## Licence

The map is under [CC BY 4.0](LICENSE). You may copy, change and share it, also in your own tools and patches, if you credit "CM 01/02 function map, github.com/maxevans60/cm0102-function-map".

[AI-LICENSE.md](AI-LICENSE.md) gives full permission for any use with AI, machine learning and large language models: training, datasets, agents and AI-built tools. That use needs no permission and no credit.

This is an unofficial fan project. It is not affiliated with or endorsed by Sports Interactive, SEGA, Eidos or Square Enix. Championship Manager is a trademark of Square Enix.
