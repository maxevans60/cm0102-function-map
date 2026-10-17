# rb_france.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ddcc0 | 22 | `RbFrance::RbFrance` | thiscall(RbFrance *this, FILE *file), ret 4 | Constructs the French ruling body on the RulingBody base and sets its kind, rule set index, nation and continent fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7ddd10 | 325 (+10 unwind) | `RbFrance::process_match_cards` | thiscall(RbFrance *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies French card rules to one player after a match: a points ban for a red card and one match for repeated bookings. | high | opus |  |
| 0x7de1a0 | 47 | `RbFrance::get_name` | thiscall(RbFrance *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the French nationality adjective into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
| 0x7de260 | 47 | `RbFrance::is_one_booking_from_ban` | thiscall(RbFrance *this unused, DisciplineEntry *entry, char *out_matches, char *out_code, int comp_id), ret 0x10 | Reports whether the player's recent French booking history means one more booking brings a ban, and sets the ban length to one match. | high | opus | 2026-10-16-sweep-rulebooks.md |
