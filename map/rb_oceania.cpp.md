# rb_oceania.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e13d0 | 21 | `RbOceania::RbOceania` | thiscall(RbOceania* this, FILE* file) returning this, ret 4 | Constructs the Oceanian ruling body on the RulingBody base, sets vtable 0x96ed74, rule set id 0x23 and its nation fields. | high | opus |  |
| 0x7e1420 | 98 (+1 unwind) | `RbOceania::process_match_cards` | thiscall(RbOceania* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Oceanian rules, banning him one match after a red card and one match for each third booking. | high | opus |  |
| 0x7e1570 | 40 | `RbOceania::get_name` | thiscall(RbOceania* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Oceanian continent name into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
