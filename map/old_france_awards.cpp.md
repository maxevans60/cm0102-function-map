# old_france_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x79dcf0 | 40 (+1 unwind) | `OldFranceAwards::OldFranceAwards` | thiscall(OldFranceAwards* this, FILE* save) ret 4, returns this | Constructs the old-format France awards object on the NationAwards base, then loads saved awards or creates fresh ones. | high | opus |  |
| 0x79dd80 | 449 (+14 unwind) | `OldFranceAwards::init_awards` | thiscall(OldFranceAwards* this, FILE* save) ret 4 | Allocates the table of fourteen old France awards with year awards and the awards of the two French divisions. | high | opus |  |
| 0x79e330 | 221 | `OldFranceAwards::daily_update` | thiscall(OldFranceAwards* this, Date* today) ret 4 | Gives French player awards on 20 November and the season awards of the two divisions on 6 May, then runs the base update. | high | opus |  |
| 0x79e560 | 12 | `OldFranceAwards::update_team_of_the_week` | thiscall(OldFranceAwards* this, TeamAward* award) ret 4 | Builds the team of the week when the given award is one of the two old France division team awards. | high | opus |  |
