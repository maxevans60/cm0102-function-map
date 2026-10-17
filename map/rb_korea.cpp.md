# rb_korea.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e0730 | 22 | `RbKorea::RbKorea` | thiscall(RbKorea* this, FILE* file) returning this, ret 4 | Constructs the Korean ruling body on the RulingBody base, sets vtable 0x96ecf4, rule set id 0x2a and the Korea nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e0780 | 163 (+4 unwind) | `RbKorea::process_match_cards` | thiscall(RbKorea* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies match cards under Korean rules, with a ban and points ban for a red card, and a ban at odd bookings from three. | high | opus |  |
| 0x7e09e0 | 47 | `RbKorea::get_name` | thiscall(RbKorea* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Korean nationality adjective into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7e0aa0 | 24 | `RbKorea::is_one_booking_from_ban` | thiscall(RbKorea* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Korean rules, true when the booking count is two, five, eight and so on. | high | opus | 2026-10-16-sweep-rulebooks.md |
