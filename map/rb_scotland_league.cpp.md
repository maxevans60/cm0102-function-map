# rb_scotland_league.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e2470 | 22 | `RbScotlandLeague::RbScotlandLeague` | thiscall(RbScotlandLeague* this, FILE* file) returning this, ret 4 | Constructs the Scottish league ruling body on the RulingBody base, sets vtable 0x96ee14, rule set id 0x18 and its nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e24c0 | 192 (+2 unwind) | `RbScotlandLeague::process_match_cards` | thiscall(RbScotlandLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Adds disciplinary points for a player's cards by offence type to his Scottish record and bans him for each sixteen points, starting fourteen days later. | high | opus |  |
| 0x7e2720 | 105 (+1 unwind) | `RbScotlandLeague::check_points_ban` | thiscall(RbScotlandLeague* this, int staff_index, Fixture* fixture) returning int, ret 8 | Converts each sixteen disciplinary points in the player's Scottish record into a ban starting today and returns one when it adds a ban. | high | sonnet |  |
| 0x7e2890 | 38 | `RbScotlandLeague::get_name` | thiscall(RbScotlandLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Scottish league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e2930 | 31 | `RbScotlandLeague::is_one_booking_from_ban` | thiscall(RbScotlandLeague* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int comp_id) returning bool, ret 0x10 | Reports whether two more disciplinary points reach the Scottish sixteen point threshold and gives the ban length that would follow. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e2980 | 37 | `RbScotlandLeague::start_new_season` | thiscall(RbScotlandLeague* this) in ECX, no stack arguments, ret 0 | Rolls each Scottish discipline entry into a new season, shifting the season ban counts into history and clearing the current count and points. | high | opus |  |
