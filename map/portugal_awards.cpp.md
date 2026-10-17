# portugal_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7d3630 | 40 (+1 unwind) | `PortugalAwards::PortugalAwards` | thiscall(PortugalAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the Portuguese awards object for its nation, loads saved awards or creates them fresh. | high | opus |  |
| 0x7d36c0 | 395 (+12 unwind) | `PortugalAwards::init_awards` | thiscall(PortugalAwards* this, FILE* load_source or 0) ret 4 | Creates the Portuguese year and team awards for the first and second divisions and stores them in the award list. | high | opus |  |
| 0x7d3be0 | 148 | `PortugalAwards::daily_update` | thiscall(PortugalAwards* this, Date* date) ret 4 | On the end-of-season date, gives player, team and manager of the year awards for both divisions, then runs the base daily update. | high | opus |  |
| 0x7d3d60 | 12 | `PortugalAwards::update_team_of_the_week` | thiscall(PortugalAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the award is one of the two Portuguese team of the week awards. | high | opus |  |
