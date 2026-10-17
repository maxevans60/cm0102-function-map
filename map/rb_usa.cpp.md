# rb_usa.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e40f0 | 23 | `RbUsa::RbUsa` | thiscall(RbUsa* this, FILE* file) returning this, ret 4 | Constructs the United States ruling body on the RulingBody base, sets vtable 0x96ef14, rule set id 0x1e and the USA nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e4140 | 129 (+1 unwind) | `RbUsa::process_match_cards` | thiscall(RbUsa* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Adds disciplinary points for a player's bookings to his US record and bans him past twenty points or for a red card, posting the ban news. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e42f0 | 38 | `RbUsa::get_name` | thiscall(RbUsa* this unused, char* buf, int buf_len, int form) ret 0xc | Writes United States into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e4390 | 13 | `RbUsa::is_one_booking_from_ban` | thiscall(RbUsa* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int unused) returning bool, ret 0x10 | Reports whether one more booking bans the player under US rules, which holds when his disciplinary points stand at exactly twenty. | high | opus | 2026-10-16-sweep-rulebooks.md |
