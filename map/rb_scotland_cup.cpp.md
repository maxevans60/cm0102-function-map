# rb_scotland_cup.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e21a0 | 22 | `RbScotlandCup::RbScotlandCup` | thiscall(RbScotlandCup* this, FILE* file) returning this, ret 4 | Constructs the Scottish cup ruling body on the RulingBody base, sets vtable 0x96edf4, rule set id 0x19 and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e21f0 | 130 (+1 unwind) | `RbScotlandCup::process_match_cards` | thiscall(RbScotlandCup* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Scottish cup rules, banning him per second booking and adding red card points to his Scottish league tally. | high | opus |  |
| 0x7e23a0 | 38 | `RbScotlandCup::get_name` | thiscall(RbScotlandCup* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Scottish cup into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e2440 | 17 | `RbScotlandCup::is_one_booking_from_ban` | thiscall(RbScotlandCup* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Scottish cup rules, which holds once he carries one booking. | high | opus | 2026-10-16-sweep-rulebooks.md |
