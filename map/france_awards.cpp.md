# france_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5c0980 | 46 (+1 unwind) | `FranceAwards::FranceAwards` | thiscall(FranceAwards* this, FILE* save) ret 4, returns this | Constructs the French awards object on the NationAwards base, then loads saved awards or creates fresh ones. | high | opus |  |
| 0x5c0a20 | 648 (+21 unwind) | `FranceAwards::init_awards` | thiscall(FranceAwards* this, FILE* save) ret 4 | Allocates the table of 21 French awards and creates its year awards and the team awards of the three French divisions. | high | opus |  |
| 0x5c1260 | 287 | `FranceAwards::daily_update` | thiscall(FranceAwards* this, Date* today) ret 4 | Gives French player awards on 20 December and the season awards of the three divisions on 6 June, then runs the base update. | high | opus |  |
| 0x5c1540 | 14 | `FranceAwards::update_team_of_the_week` | thiscall(FranceAwards* this, TeamAward* award) ret 4 | Builds the team of the week when the given award is one of the three French division team awards. | high | opus |  |
