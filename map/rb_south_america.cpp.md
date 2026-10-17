# rb_south_america.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e29e0 | 21 | `RbSouthAmerica::RbSouthAmerica` | thiscall(RbSouthAmerica* this, FILE* file) returning this, ret 4 | Constructs the South American ruling body on the RulingBody base, sets vtable 0x96ee34, rule set id 2 and the South American continent field. | high | opus | 2026-10-16-research-name-check.md |
| 0x7e2a30 | 99 (+1 unwind) | `RbSouthAmerica::process_match_cards` | thiscall(RbSouthAmerica* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under South American rules, banning him after a red card or each second booking and posting the ban news. | high | opus |  |
| 0x7e2b90 | 40 | `RbSouthAmerica::get_name` | thiscall(RbSouthAmerica* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the South American continent name into the buffer as the ruling body name, or shows a version error when the buffer is under twenty. | high | opus |  |
