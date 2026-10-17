# rb_ireland.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7df480 | 22 | `RbIreland::RbIreland` | thiscall(RbIreland *this, FILE *file), ret 4 | Constructs the Irish ruling body on the RulingBody base and sets its kind, rule set index, nation and continent fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7df4d0 | 260 (+7 unwind) | `RbIreland::process_match_cards` | thiscall(RbIreland *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies Irish card rules to one player after a match, with rising bans from the fifth booking that start fourteen days later. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7df850 | 47 | `RbIreland::get_name` | thiscall(RbIreland *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the Irish nationality adjective into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
| 0x7df910 | 29 | `RbIreland::is_one_booking_from_ban` | thiscall(RbIreland *this unused, DisciplineEntry *entry, char *out_matches, char *out_code, int comp_id), ret 0x10 | Reports whether the player's booking count is one short of an Irish ban threshold, and sets the ban length to one match. | high | opus | 2026-10-16-sweep-rulebooks.md |
