# CM 01/02 function map

A map of every function in `cm0102.exe` 3.9.68, the last official patch of Championship Manager 01/02. Each of the 6,863 game and library functions has its address, the source file it came from, a name, its calling convention and one sentence on what it does.

Search it by address or by word: **https://maxevans60.github.io/cm0102-function-map/**

The map came out of the [Bosman Edition](https://github.com/maxevans60/cm0102-bosman-edition), a recompiled port of the game to Mac, Windows and Linux. It is free for anyone who patches, mods or studies the game.

## Look up an address

The map uses the addresses that OllyDbg and x64dbg show, written as `0x8e7810`. Olly shows the same address as `008E7810`.

- An address from a patch list is often a file offset. Add 0x400000 to it, or tick "file offset" on the search page.
- Most patch addresses lie inside a function. The search page shows the function that holds the address.
- The search also takes a word, such as `loan`, `prize` or `League::`.

## Files

| File | What it holds |
|---|---|
| [`map/index.md`](map/index.md) | Every source file with its number of functions |
| `map/<file>.cpp.md` | One page for each source file: address, size, name, convention, purpose, confidence |
| [`map/functions.tsv`](map/functions.tsv) | All named functions with every column, for scripts and spreadsheets |
| [`map/names.tsv`](map/names.tsv) | Address, file, name, confidence, model and the research docs that cite it |
| [`map/not-high.tsv`](map/not-high.tsv) | Every row that is not high, with one line on what is missing for high |
| [`map/function-files.tsv`](map/function-files.tsv) | All 11,747 function starts, unwind funclets and runtime code included, with their file |

The source file names come from the assert strings in the exe, such as `E:\dev\CM3\cm3 00-01\cm3\code\comp\leagues\league.cpp`. A function without an assert of its own gets the file of the code around it. A competition class keeps the method names of its base class for each vtable slot, so `SweCup::update_staff_records_for_status` is slot 17 of the cup vtable.

## How the map was made

AI agents (Claude Opus, and Sonnet for 254 library functions) read each function. They read its strings, asserts, callers, callees, vtable slots and decompiled code, and gave it a name. Then fresh agents reviewed every name with medium or low confidence, every shared stub and every false entry. A third agent settled each disagreement. The review changed 842 names. A confidence pass then gave the agents the names of the globals and of the reviewed neighbours, and checked the medium and low rows again. It raised 245 rows to high and changed 10 names.

Each row has a confidence:

- **high** (5,702): the evidence quotes a string, a caller or a vtable slot that pins the purpose.
- **medium** (1,133): the shape of the code and the callers agree, but no single fact proves the name.
- **low** (28): a guess.

Read the code before you build a patch on a medium or low name. A name helps you find code. It does not prove what the code does.

## What the map holds

The map holds names, file names and short descriptions. It holds no code, decompiled code or data of the original game. To read the code you need your own copy of the game. Eidos made it free in 2008.

A data map of the globals in the same style is planned: the competition ids, the database counts and the record fields.

## Report a wrong name

Open an issue with the address, the name you think is right and what the code does. A caller, a string or a field offset helps most. The map is generated from the Bosman Edition repo, so a pull request that edits `map/` would be overwritten. The fix goes into the next update of the map.

## Licence

The map is under [CC BY 4.0](LICENSE). You may copy, change and share it, also in your own tools and patches, if you credit "CM 01/02 function map, github.com/maxevans60/cm0102-function-map".

[AI-LICENSE.md](AI-LICENSE.md) gives full permission for any use with AI, machine learning and large language models: training, datasets, agents and AI-built tools. That use needs no permission and no credit.

This is an unofficial fan project. It is not affiliated with or endorsed by Sports Interactive, SEGA, Eidos or Square Enix. Championship Manager is a trademark of Square Enix.
