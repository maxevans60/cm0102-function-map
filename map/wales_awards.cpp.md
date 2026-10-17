# wales_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x90ead0 | 82 (+2 unwind) | `WalesAwards::WalesAwards` | thiscall(WalesAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the Welsh awards on NationAwards, sets the Wales nation record, then loads saved awards or creates the month ratings and award table. | high | opus |  |
| 0x90ec10 | 230 (+6 unwind) | `WalesAwards::init_awards` | thiscall(WalesAwards* this, FILE* load_source or 0) ret 4 | Allocates the six-award table and creates one team award, four year awards and one month award for Wales. | high | opus |  |
| 0x90ef10 | 100 | `WalesAwards::daily_update` | thiscall(WalesAwards* this, Date* date) ret 4 | On day 11 of month index 4, gives the Welsh year awards, then advances the month award slots and runs the base update. | high | opus |  |
| 0x90f020 | 23 | `WalesAwards::on_month_change` | thiscall(WalesAwards* this) ret 0, this not read | Gives the Welsh manager of the month award to the best staff record of the competition at 0x9cf94c. | high | opus |  |
| 0x90f060 | 13 | `WalesAwards::update_team_of_the_week` | thiscall(WalesAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week nominations when the given team award is the first award in the award table. | high | opus |  |
