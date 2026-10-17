# rb_belgium_league.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dbca0 | 25 | `RbBelgiumLeague::RbBelgiumLeague` | thiscall(RbBelgiumLeague* this, FILE* file) returning this, ret 4 | Constructs the Belgian league ruling body on the RulingBody base, sets vtable 0x96ea74, rule set id 4 and the Belgium nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dbcf0 | 204 (+4 unwind) | `RbBelgiumLeague::process_match_cards` | thiscall(RbBelgiumLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Belgian league rules, queueing a points ban for a red card and banning him at each third booking. | high | opus |  |
| 0x7dbfe0 | 38 | `RbBelgiumLeague::get_name` | thiscall(RbBelgiumLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Belgian league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
