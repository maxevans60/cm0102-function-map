# rb_italy_cup.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7df960 | 22 | `RbItalyCup::RbItalyCup` | thiscall(RbItalyCup* this, FILE* file) returning this, ret 4 | Constructs the Italian cup ruling body on the RulingBody base, sets vtable 0x96ec74, rule set id 0x12 and the Italy nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7df9b0 | 195 (+6 unwind) | `RbItalyCup::process_match_cards` | thiscall(RbItalyCup* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Italian cup rules, banning him for a red card and at each second booking, and queueing a points ban. | high | opus |  |
| 0x7dfc90 | 38 | `RbItalyCup::get_name` | thiscall(RbItalyCup* this unused, char* buf, int buf_len, int form) ret 0xc | Writes "Italian cup" into the buffer as the ruling body name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7dfd30 | 21 | `RbItalyCup::is_one_booking_from_ban` | thiscall(RbItalyCup* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Italian cup rules, true when the booking count is odd, with a one match ban. | high | opus | 2026-10-16-sweep-rulebooks.md |
