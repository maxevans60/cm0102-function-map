# rb_turkey_league.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e3d60 | 22 | `RbTurkeyLeague::RbTurkeyLeague` | thiscall(RbTurkeyLeague* this, FILE* file) returning this, ret 4 | Constructs the Turkish league ruling body on the RulingBody base, sets vtable 0x96eef4, rule set id 0x25 and the Turkey nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e3db0 | 163 (+5 unwind) | `RbTurkeyLeague::process_match_cards` | thiscall(RbTurkeyLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Turkish league rules, queueing a points ban for a red card and banning him at each fourth booking. | high | opus |  |
| 0x7e4010 | 38 | `RbTurkeyLeague::get_name` | thiscall(RbTurkeyLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Turkish league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e40b0 | 21 | `RbTurkeyLeague::is_one_booking_from_ban` | thiscall(RbTurkeyLeague* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int unused) returning bool, ret 0x10 | Reports whether one more booking bans the player under Turkish rules, which holds when his booking count plus one is a multiple of four. | high | opus | 2026-10-16-sweep-rulebooks.md |
