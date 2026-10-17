# usa_rules.cpp: 2 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x90b940 | 81 (+1 unwind) | `USA_RULES::USA_RULES` | thiscall(USA_RULES* this, 5 args forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the USA transfer rules, sets vtable 0x970a38, allocates the 12-byte transfer window table and sets byte +0x13 to 4. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x90ba60 | 17 | `USA_RULES::fill_squad_restrictions` | thiscall(USA_RULES* this, competition_t* competition, u8* record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and allows four foreign players except in competition 0x9cf690. | high | opus | 2026-10-16-sweep-rulebooks.md |
