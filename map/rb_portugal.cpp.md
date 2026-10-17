# rb_portugal.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e1a60 | 22 | `RbPortugal::RbPortugal` | thiscall(RbPortugal* this, FILE* file) returning this, ret 4 | Constructs the Portuguese ruling body on the RulingBody base, sets vtable 0x96edb4, rule set id 0x17 and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e1ab0 | 157 (+4 unwind) | `RbPortugal::process_match_cards` | thiscall(RbPortugal* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Portuguese rules, queueing a red card points ban from the next day and banning him at each fifth booking. | high | opus |  |
| 0x7e1cf0 | 47 | `RbPortugal::get_name` | thiscall(RbPortugal* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Portuguese nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e1db0 | 29 | `RbPortugal::is_one_booking_from_ban` | thiscall(RbPortugal* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Portuguese rules, using a step of three bookings in one competition and five elsewhere. | high | opus | 2026-10-16-sweep-rulebooks.md |
