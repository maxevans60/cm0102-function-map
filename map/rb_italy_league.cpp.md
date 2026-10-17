# rb_italy_league.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dfd70 | 22 | `RbItalyLeague::RbItalyLeague` | thiscall(RbItalyLeague* this, FILE* file) returning this, ret 4 | Constructs the Italian league ruling body on the RulingBody base, sets vtable 0x96ec94, rule set id 0x11 and the Italy nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dfdc0 | 212 (+6 unwind) | `RbItalyLeague::process_match_cards` | thiscall(RbItalyLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Italian league rules, banning him for a red card and at the fourth, seventh and odd bookings from nine. | high | opus |  |
| 0x7e00c0 | 38 | `RbItalyLeague::get_name` | thiscall(RbItalyLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes "Italian league" into the buffer as the ruling body name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7e0160 | 27 | `RbItalyLeague::is_one_booking_from_ban` | thiscall(RbItalyLeague* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether one more booking bans the player under Italian league rules, at three, six or an even count from eight. | high | opus | 2026-10-16-sweep-rulebooks.md |
