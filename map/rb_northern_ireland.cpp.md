# rb_northern_ireland.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e0af0 | 22 | `RbNorthernIreland::RbNorthernIreland` | thiscall(RbNorthernIreland* this, FILE* file) returning this, ret 4 | Constructs the Northern Irish ruling body on the RulingBody base, sets vtable 0x96ed14, rule set id 0x24 and the Northern Ireland nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e0b40 | 158 (+2 unwind) | `RbNorthernIreland::process_match_cards` | thiscall(RbNorthernIreland* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Adds card points under Northern Irish rules and bans the player for one, two, four or six matches at 20, 32, 42 and 51 points. | high | opus |  |
| 0x7e0d60 | 47 | `RbNorthernIreland::get_name` | thiscall(RbNorthernIreland* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Northern Irish nationality adjective into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7e0e20 | 48 | `RbNorthernIreland::is_one_booking_from_ban` | thiscall(RbNorthernIreland* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking takes the player over a Northern Irish threshold, and gives a ban length of one, two, four or six matches. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e0ec0 | 15 | `RbNorthernIreland::start_new_season` | thiscall(RbNorthernIreland* this) ret 0 | Clears the disciplinary points of every discipline entry of the Northern Irish ruling body at the start of a season. | high | opus |  |
