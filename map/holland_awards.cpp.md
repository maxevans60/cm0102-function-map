# holland_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5f8fe0 | 40 (+1 unwind) | `HollandAwards::HollandAwards` | thiscall(HollandAwards* this, FILE* load_source or 0), ret 4, returns this | Constructs the Dutch awards object on NationAwards, sets its nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x5f9070 | 336 (+10 unwind) | `HollandAwards::init_awards` | thiscall(HollandAwards* this, FILE* load_source or 0), ret 4 | Allocates the table of ten Dutch awards and creates each year award and team award for the two national divisions. | high | opus |  |
| 0x5f94c0 | 163 | `HollandAwards::daily_update` | thiscall(HollandAwards* this, Date* date), ret 4 | Gives the Dutch top player awards on 20/11 and the year awards on 25/2 (zero-based months), then runs the base update. | high | opus |  |
| 0x5f9670 | 12 | `HollandAwards::update_team_of_the_week` | thiscall(HollandAwards* this, TEAM_AWARD* award), ret 4 | Builds the team of the week for an award when it is one of the two Dutch team awards. | high | opus |  |
