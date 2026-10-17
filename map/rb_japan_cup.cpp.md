# rb_japan_cup.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e01b0 | 21 | `RbJapanCup::RbJapanCup` | thiscall(RbJapanCup* this, FILE* file) returning this, ret 4 | Constructs the Japanese cup ruling body on the RulingBody base, sets vtable 0x96ecb4, rule set id 0x14 and the Japan nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e0200 | 133 (+1 unwind) | `RbJapanCup::process_match_cards` | thiscall(RbJapanCup* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Japanese cup rules, banning him at each second booking and for one to four matches by red card offence. | high | opus |  |
| 0x7e03b0 | 38 | `RbJapanCup::get_name` | thiscall(RbJapanCup* this unused, char* buf, int buf_len, int form) ret 0xc | Writes "Japanese cup" into the buffer as the ruling body name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7e0450 | 21 | `RbJapanCup::is_one_booking_from_ban` | thiscall(RbJapanCup* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under every second booking rules, true when the booking count is odd, with a one match ban. | high | opus | 2026-10-16-sweep-rulebooks.md |
