# rb_asia.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7db360 | 21 | `RbAsia::RbAsia` | thiscall(RbAsia* this, FILE* file) returning this, ret 4 | Constructs the Asian ruling body on the RulingBody base, sets vtable 0x96ea14, rule set id 0x29 and the Asian continent field. | high | opus |  |
| 0x7db3b0 | 101 (+1 unwind) | `RbAsia::process_match_cards` | thiscall(RbAsia* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Asian rules, banning him after a red card or each second booking and posting the ban news. | high | opus |  |
| 0x7db510 | 40 | `RbAsia::get_name` | thiscall(RbAsia* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Asian continent name into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
