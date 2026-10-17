# rb_wales.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e43c0 | 22 | `RbWales::RbWales` | thiscall(RbWales* this, FILE* file) returning this, ret 4 | Constructs the Welsh ruling body on the RulingBody base, sets vtable 0x96ef34, rule set id 0x28 and the Wales nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e4410 | 157 (+4 unwind) | `RbWales::process_match_cards` | thiscall(RbWales* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Welsh rules, banning him after a red card or each fifth booking and posting the ban news. | high | opus |  |
| 0x7e4650 | 47 | `RbWales::get_name` | thiscall(RbWales* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Welsh nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e4710 | 20 | `RbWales::is_one_booking_from_ban` | thiscall(RbWales* this unused, DisciplineEntry* entry, char* out_matches, char* out_code, int comp_id) returning bool, ret 0x10 | Reports whether the player's next booking is a fifth, and so brings a ban, and sets the ban length to one match. | high | opus | 2026-10-16-sweep-rulebooks.md |
