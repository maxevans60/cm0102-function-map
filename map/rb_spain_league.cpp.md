# rb_spain_league.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e2f80 | 22 | `RbSpainLeague::RbSpainLeague` | thiscall(RbSpainLeague* this, FILE* file) returning this, ret 4 | Constructs the Spanish league ruling body on the RulingBody base, sets vtable 0x96ee74, rule set id 0x1a and the Spain nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e2fd0 | 162 (+5 unwind) | `RbSpainLeague::process_match_cards` | thiscall(RbSpainLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Spanish league rules, queueing a points ban for a red card and banning him at each fifth booking. | high | opus |  |
| 0x7e3230 | 38 | `RbSpainLeague::get_name` | thiscall(RbSpainLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Spanish league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
