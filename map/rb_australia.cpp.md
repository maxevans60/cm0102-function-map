# rb_australia.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7db5b0 | 22 | `RbAustralia::RbAustralia` | thiscall(RbAustralia* this, FILE* file) returning this, ret 4 | Constructs the Australian ruling body on the RulingBody base, sets vtable 0x96ea34, rule set id 0x22 and the Australia nation fields. | high | opus | 2026-10-16-sweep-international.md, 2026-10-16-sweep-rulebooks.md |
| 0x7db600 | 130 (+3 unwind) | `RbAustralia::process_match_cards` | thiscall(RbAustralia* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Australian rules, banning him at the fifth booking and every second one after, and for red cards. | high | opus |  |
| 0x7db7e0 | 47 | `RbAustralia::get_name` | thiscall(RbAustralia* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Australian nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7db8a0 | 26 | `RbAustralia::is_one_booking_from_ban` | thiscall(RbAustralia* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int unused) returning bool, ret 0x10 | Reports whether one more booking bans the player under Australian rules, at four bookings or an even count from six. | high | opus | 2026-10-16-sweep-rulebooks.md |
