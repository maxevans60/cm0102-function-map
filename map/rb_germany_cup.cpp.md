# rb_germany_cup.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7de2e0 | 22 | `RbGermanyCup::RbGermanyCup` | thiscall(RbGermanyCup *this, FILE *file), ret 4 | Constructs the German cup ruling body on the RulingBody base and sets its kind, rule set index, nation and continent fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7de330 | 158 (+4 unwind) | `RbGermanyCup::process_match_cards` | thiscall(RbGermanyCup *this, MatchPlayer *player, Fixture *fixture), ret 8 | Applies German cup card rules to one player after a match: one match ban every fifth booking, points ban for a red card. | high | opus |  |
| 0x7de580 | 38 | `RbGermanyCup::get_name` | thiscall(RbGermanyCup *this unused, char *buf, int buf_len, int flag), ret 0xc | Writes the text German cup into the buffer as the ruling body name, or reports an assert when the buffer is too short. | high | opus |  |
