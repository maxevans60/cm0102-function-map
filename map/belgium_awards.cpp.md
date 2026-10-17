# belgium_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x424480 | 40 (+1 unwind) | `BelgiumAwards::BelgiumAwards` | thiscall(BelgiumAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the Belgian awards object on NationAwards, sets its nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x424510 | 365 (+11 unwind) | `BelgiumAwards::init_awards` | thiscall(BelgiumAwards* this, FILE* load_source or 0) ret 4 | Allocates the table of eleven Belgian awards and creates each year award and team award, reporting an error when the table allocation fails. | high | opus |  |
| 0x4249c0 | 159 | `BelgiumAwards::daily_update` | thiscall(BelgiumAwards* this, Date* date) ret 4 | Gives the Belgian top player awards on 29 November and the year awards on 6 May, then runs the base update. | high | opus |  |
| 0x424b60 | 14 | `BelgiumAwards::update_team_of_the_week` | thiscall(BelgiumAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week for an award when it is one of the three Belgian team awards. | high | opus |  |
