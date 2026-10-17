# norway_awards.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x793940 | 82 (+2 unwind) | `NorwayAwards::NorwayAwards` | thiscall(NorwayAwards* this, FILE* save) ret 4, returns this | Constructs the Norway awards object on the NationAwards base, then loads saved awards or creates the month ratings and award table. | high | opus |  |
| 0x793a80 | 641 (+19 unwind) | `NorwayAwards::init_awards` | thiscall(NorwayAwards* this, FILE* save) ret 4 | Allocates the table of eleven Norway awards and creates its year awards, team awards and month awards for the two Norwegian leagues. | high | opus |  |
| 0x794220 | 43 | `NorwayAwards::init_awards_fragment_794220` | none (fragment of 0x793a80), ret 4 | Stores the two month awards of the second Norwegian league in award table slots 9 and 10 as the last part of NorwayAwards::init_awards. | high | opus |  |
| 0x7942c0 | 136 | `NorwayAwards::daily_update` | thiscall(NorwayAwards* this, Date* today) ret 4 | Gives the five Norway player awards on 20 October, advances the month award slots at season start and runs the base daily update. | high | opus |  |
| 0x794430 | 54 | `NorwayAwards::on_month_change` | thiscall(NorwayAwards* this) ret 0 | Gives the manager of the month awards for the two Norwegian leagues and the two monthly player awards from the month ratings. | high | opus |  |
| 0x7944d0 | 12 | `NorwayAwards::update_team_of_the_week` | thiscall(NorwayAwards* this, TeamAward* award) ret 4 | Builds the team of the week when the given award is one of the two Norwegian league team awards. | high | opus |  |
