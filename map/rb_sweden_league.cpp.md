# rb_sweden_league.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e3650 | 22 | `RbSwedenLeague::RbSwedenLeague` | thiscall(RbSwedenLeague* this, FILE* file) returning this, ret 4 | Constructs the Swedish league ruling body on the RulingBody base, sets vtable 0x96eeb4, rule set id 0x1c and the Sweden nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7e36a0 | 170 (+5 unwind) | `RbSwedenLeague::process_match_cards` | thiscall(RbSwedenLeague* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Swedish league rules, queueing a points ban for a red card and banning him at the third booking and each second one after. | high | opus |  |
| 0x7e3920 | 38 | `RbSwedenLeague::get_name` | thiscall(RbSwedenLeague* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Swedish league into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
| 0x7e39c0 | 24 | `RbSwedenLeague::is_one_booking_from_ban` | thiscall(RbSwedenLeague* this unused, DisciplineEntry* entry, char* out_ban_length, char* out_flag, int unused) returning bool, ret 0x10 | Reports whether one more booking bans the player under Swedish rules, which holds when his booking count is even and not zero. | high | opus | 2026-10-16-sweep-rulebooks.md |
