# russia_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ec210 | 40 (+1 unwind) | `RussiaAwards::RussiaAwards` | thiscall(RussiaAwards* this, FILE* file) ret 4, returns this | Constructs the Russian awards object on NationAwards, sets its nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x7ec2a0 | 259 (+7 unwind) | `RussiaAwards::init_awards` | thiscall(RussiaAwards* this, FILE* file) ret 4 | Allocates the seven-award table and creates the player of the year award plus two team awards and a month award for each Russian division. | high | opus |  |
| 0x7ec600 | 56 | `RussiaAwards::daily_update` | thiscall(RussiaAwards* this, Date* date) ret 4 | On day 30 of month index 10, gives the Russian player of the year and both teams of the season, then runs the base update. | high | opus |  |
| 0x7ec6a0 | 12 | `RussiaAwards::update_team_of_the_week` | thiscall(RussiaAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week for an award when it is one of the two Russian weekly team awards. | high | opus |  |
| 0x7ec6c0 | 64 | `RussiaAwards::on_month_change` | thiscall(RussiaAwards* this) ret 0 | Gives the player of the month award of the Premier League and of the First Division from the month ratings, except in month index 5. | high | opus |  |
