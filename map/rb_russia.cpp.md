# rb_russia.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e1e00 | 22 | `RbRussia::RbRussia` | thiscall(RbRussia* this, FILE* file) returning this, ret 4 | Constructs the Russian ruling body on the RulingBody base, sets vtable 0x96edd4, rule set id 0x27 and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e1e50 | 162 (+6 unwind) | `RbRussia::process_match_cards` | thiscall(RbRussia* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Russian rules, counting bookings in cycles of four and giving a red card one match plus a points ban. | high | opus |  |
| 0x7e20b0 | 47 | `RbRussia::get_name` | thiscall(RbRussia* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Russian nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e2170 | 13 | `RbRussia::is_one_booking_from_ban` | thiscall(RbRussia* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking completes the player's Russian four booking cycle, which holds when his booking count is three. | high | opus | 2026-10-16-sweep-rulebooks.md |
