# rb_norway_league.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e1150 | 22 | `RbNorwayLeague::RbNorwayLeague` | thiscall(RbNorwayLeague* this, FILE* file) returning this, ret 4 | Constructs the Norwegian league ruling body on the RulingBody base, sets vtable 0x96ed54, rule set id 0x15 and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e11a0 | 97 (+1 unwind) | `RbNorwayLeague::process_match_cards` | thiscall(RbNorwayLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Norwegian league rules, banning him one match for a red card, the third booking and each from the fifth. | high | opus |  |
| 0x7e12f0 | 38 | `RbNorwayLeague::get_name` | thiscall(RbNorwayLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Norwegian league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e1390 | 18 | `RbNorwayLeague::is_one_booking_from_ban` | thiscall(RbNorwayLeague* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Norwegian league rules, which holds when his booking count is two or at least four. | high | opus | 2026-10-16-sweep-rulebooks.md |
