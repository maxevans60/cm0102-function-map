# rb_international.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7df180 | 20 | `RbInternational::RbInternational` | thiscall(RbInternational *this, FILE *file), ret 4 | Constructs the international ruling body on the RulingBody base with no nation or continent and sets its kind and rule set index. | high | opus | 2026-10-16-sweep-international.md |
| 0x7df1c0 | 101 (+1 unwind) | `RbInternational::process_match_cards` | thiscall(RbInternational *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies international card rules for one player after a match, with a one match ban for a red card and for every second booking. | high | opus |  |
| 0x7df320 | 38 | `RbInternational::get_name` | thiscall(RbInternational *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the text International into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
| 0x7df3c0 | 70 | `RbInternational::start_new_season` | thiscall(RbInternational *this), ret 0 | Clears idle international discipline entries and releases bans older than three years at the start of a season, then compacts the list. | high | opus |  |
