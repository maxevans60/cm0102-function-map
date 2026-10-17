# england_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x578780 | 82 (+2 unwind) | `EnglandAwards::EnglandAwards` | thiscall(EnglandAwards* this, FILE* file) ret 4, returns this | Builds the England awards object, loads it from a save file when one is given, or creates its month ratings and award objects. | high | opus |  |
| 0x5788c0 | 1039 (+32 unwind) | `EnglandAwards::init_awards` | thiscall(EnglandAwards* this, FILE* file) ret 4 | Allocates the award table and constructs the yearly, monthly and team awards of each English division, adding the Conference awards when it exists. | high | opus |  |
| 0x579610 | 247 | `EnglandAwards::daily_update` | thiscall(EnglandAwards* this, Date* date) ret 4 | Gives the yearly player, team and manager awards on fixed dates and moves the month award slots on at the nation's season change. | high | opus |  |
| 0x579900 | 165 | `EnglandAwards::on_month_change` | thiscall(EnglandAwards* this) ret 0 | Gives the manager of the month award of each English division, and the Conference when played, then the player of the month awards. | high | opus |  |
| 0x579af0 | 23 | `EnglandAwards::update_team_of_the_week` | thiscall(EnglandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week nominations when the given award is the team award of one of the English divisions. | high | opus |  |
