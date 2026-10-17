# rb_greece.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7de960 | 22 | `RbGreece::RbGreece` | thiscall(RbGreece *this, FILE *file), ret 4 | Constructs the Greek ruling body on the RulingBody base and sets its kind, rule set index, nation and continent fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7de9b0 | 197 (+6 unwind) | `RbGreece::process_match_cards` | thiscall(RbGreece *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies Greek card rules to one player after a match: one match ban every third booking, points ban for a red card. | high | opus |  |
| 0x7dec90 | 47 | `RbGreece::get_name` | thiscall(RbGreece *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the Greek nationality adjective into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
| 0x7ded50 | 20 | `RbGreece::is_one_booking_from_ban` | thiscall(RbGreece *this unused, DisciplineEntry *entry, char *out_matches, char *out_code, int comp_id), ret 0x10 | Reports whether the player's booking count leaves him one booking short of a ban every third booking, and sets the ban length to one match. | high | opus | 2026-10-16-sweep-rulebooks.md |
