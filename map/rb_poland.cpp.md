# rb_poland.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e1610 | 22 | `RbPoland::RbPoland` | thiscall(RbPoland* this, FILE* file) returning this, ret 4 | Constructs the Polish ruling body on the RulingBody base, sets vtable 0x96ed94, rule set id 0x1f and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e1660 | 208 (+6 unwind) | `RbPoland::process_match_cards` | thiscall(RbPoland* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Polish rules, queueing a red card points ban from the next Wednesday and banning him at set booking counts. | high | opus |  |
| 0x7e1950 | 47 | `RbPoland::get_name` | thiscall(RbPoland* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Polish nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e1a10 | 30 | `RbPoland::is_one_booking_from_ban` | thiscall(RbPoland* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Polish rules, which holds at booking counts three, six, nine or odd counts above nine. | high | opus | 2026-10-16-sweep-rulebooks.md |
