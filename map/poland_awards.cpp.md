# poland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7cd130 | 40 (+1 unwind) | `PolandAwards::PolandAwards` | thiscall(PolandAwards* this, FILE* file) ret 4, returns this | Builds the Polish awards on NationAwards and loads them from the save file, or creates the award list when loading fails. | high | opus |  |
| 0x7cd1c0 | 349 (+10 unwind) | `PolandAwards::init_awards` | thiscall(PolandAwards* this, FILE* file) ret 4 | Allocates the ten-award table and builds a team award, three year awards and a month award for each of the two Polish divisions. | high | opus |  |
| 0x7cd630 | 128 | `PolandAwards::daily_update` | thiscall(PolandAwards* this, Date* date) ret 4 | On the award date gives both divisions' player and manager of the year awards, advances month award slots, then runs the base check. | high | opus |  |
| 0x7cd790 | 42 | `PolandAwards::on_month_change` | thiscall(PolandAwards* this) ret 0, this unused | Finds the best monthly record of each Polish division and stores it as the month award winner for the current month and year. | high | opus |  |
| 0x7cd810 | 12 | `PolandAwards::update_team_of_the_week` | thiscall(PolandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is one of the two Polish division team awards. | high | opus |  |
