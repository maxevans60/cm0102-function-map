# rb_japan_league.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e0490 | 22 | `RbJapanLeague::RbJapanLeague` | thiscall(RbJapanLeague* this, FILE* file) returning this, ret 4 | Constructs the Japanese league ruling body on the RulingBody base, sets vtable 0x96ecd4, rule set id 0x13 and the Japan nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e04e0 | 132 (+1 unwind) | `RbJapanLeague::process_match_cards` | thiscall(RbJapanLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Japanese league rules, banning him at each third booking and for one to four matches by red card offence. | high | opus |  |
| 0x7e0690 | 38 | `RbJapanLeague::get_name` | thiscall(RbJapanLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes "Japanese league" into the buffer as the ruling body name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
