# greece_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5ec850 | 40 (+1 unwind) | `GreeceAwards::GreeceAwards` | thiscall(GreeceAwards* this, void* file) ret 4, returns this | Constructs the Greek awards object on NationAwards, sets its nation record, then loads saved awards or creates them fresh. | high | opus |  |
| 0x5ec8e0 | 337 (+10 unwind) | `GreeceAwards::init_awards` | thiscall(GreeceAwards* this, void* file) ret 4 | Allocates the ten-award table and creates two national year awards, then a team award and three year awards for each Greek division. | high | opus |  |
| 0x5ecd30 | 135 | `GreeceAwards::daily_update` | thiscall(GreeceAwards* this, Date* date) ret 4 | On 30 May, gives the Greek top player awards and each division's player, manager and young player awards, then runs the base update. | high | opus |  |
| 0x5ece90 | 12 | `GreeceAwards::update_team_of_the_week` | thiscall(GreeceAwards* this, void* award) ret 4 | Builds the team of the week for an award when it is one of the two Greek divisional team awards. | high | opus |  |
