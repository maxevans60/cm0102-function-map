# rb_holland.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ded90 | 22 | `RbHolland::RbHolland` | thiscall(RbHolland *this, FILE *file), ret 4 | Constructs the Dutch ruling body on the RulingBody base and sets its kind, rule set index, nation and continent fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dede0 | 186 (+6 unwind) | `RbHolland::process_match_cards` | thiscall(RbHolland *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies Dutch card rules to one player after a match: bans at the third and each later booking from five, points ban for red. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7df090 | 47 | `RbHolland::get_name` | thiscall(RbHolland *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the Dutch nationality adjective into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
| 0x7df150 | 13 | `RbHolland::is_one_booking_from_ban` | thiscall(RbHolland *this unused, DisciplineEntry *entry, char *out_matches, char *out_code, int comp_id), ret 0x10 | Reports whether the player has two bookings and so is one booking short of a Dutch ban, and sets the ban length to one match. | high | opus | 2026-10-16-sweep-rulebooks.md |
