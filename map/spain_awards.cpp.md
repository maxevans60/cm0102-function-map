# spain_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x858ea0 | 40 (+1 unwind) | `SpainAwards::SpainAwards` | thiscall(SpainAwards* this, File* save) ret 4 | Constructs the Spanish awards on NationAwards, sets its nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x858f30 | 279 (+8 unwind) | `SpainAwards::init_awards` | thiscall(SpainAwards* this, File* save) ret 4 | Allocates the table of eight Spanish awards and creates a team award and three year awards for each of the two Spanish divisions. | high | opus |  |
| 0x8592c0 | 111 | `SpainAwards::daily_update` | thiscall(SpainAwards* this, Date* today) ret 4 | On day 16 of month index 5, gives the Spanish manager and player awards of both divisions, then runs the base update. | high | opus |  |
| 0x8593e0 | 12 | `SpainAwards::update_team_of_the_week` | thiscall(SpainAwards* this, Award* award) ret 4 | Builds the team of the week when the given award is one of the two Spanish divisional team awards. | high | opus |  |
