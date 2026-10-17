# rb_norway_cup.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e0ef0 | 22 | `RbNorwayCup::RbNorwayCup` | thiscall(RbNorwayCup* this, FILE* file) returning this, ret 4 | Constructs the Norwegian cup ruling body on the RulingBody base, sets vtable 0x96ed34, rule set id 0x16 and the Norway nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e0f40 | 91 (+1 unwind) | `RbNorwayCup::process_match_cards` | thiscall(RbNorwayCup* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Norwegian cup rules, banning him one match for a red card or for every booking from the second. | high | opus |  |
| 0x7e1080 | 38 | `RbNorwayCup::get_name` | thiscall(RbNorwayCup* this unused, char* buf, int buf_len, int form) ret 0xc | Writes "Norwegian cup" into the buffer as the ruling body name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7e1120 | 13 | `RbNorwayCup::is_one_booking_from_ban` | thiscall(RbNorwayCup* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Norwegian cup rules, true when he has one booking, with a one match ban. | high | opus | 2026-10-16-sweep-rulebooks.md |
