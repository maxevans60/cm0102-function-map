# croatia_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x517f10 | 40 (+1 unwind) | `CroatiaAwards::CroatiaAwards` | thiscall(CroatiaAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the Croatian awards object on NationAwards, sets its nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x517fa0 | 309 (+9 unwind) | `CroatiaAwards::init_awards` | thiscall(CroatiaAwards* this, FILE* load_source or 0) ret 4 | Allocates the nine-award table and creates one team award and two year awards for each of the three Croatian divisions. | high | opus | 2026-10-14-widescreen-inventory.md |
| 0x5183a0 | 118 | `CroatiaAwards::daily_update` | thiscall(CroatiaAwards* this, Date* date) ret 4 | On day 30 of month index 4, gives the two player of the year awards of each Croatian division, then runs the base update. | high | opus |  |
| 0x5184d0 | 14 | `CroatiaAwards::update_team_of_the_week` | thiscall(CroatiaAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week for an award when it is one of the three Croatian team awards. | high | opus |  |
