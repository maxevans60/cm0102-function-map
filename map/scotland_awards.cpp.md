# scotland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7f5170 | 82 (+2 unwind) | `ScotlandAwards::ScotlandAwards` | thiscall(ScotlandAwards* this, FILE* file or 0) ret 4, returns this | Builds the Scottish awards on NationAwards, sets the nation record, then loads saved awards or creates the month ratings and award objects. | high | opus |  |
| 0x7f52b0 | 873 (+27 unwind) | `ScotlandAwards::init_awards` | thiscall(ScotlandAwards* this, FILE* file or 0) ret 4 | Allocates the table of 27 Scottish awards and creates the year, month and team awards of the nation and all four divisions. | high | opus |  |
| 0x7f5dc0 | 204 | `ScotlandAwards::daily_update` | thiscall(ScotlandAwards* this, Date* date) ret 4 | Gives the yearly manager, player and team awards on 23 May, moves the month award slots at season change, then runs the base update. | high | opus |  |
| 0x7f6010 | 306 | `ScotlandAwards::on_month_change` | thiscall(ScotlandAwards* this) ret 0 | Gives each Scottish division's manager of the month award to its best staff record, then the player and young player of the month awards. | high | opus |  |
| 0x7f6360 | 16 | `ScotlandAwards::update_team_of_the_week` | thiscall(ScotlandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is the team award of one of the four Scottish divisions. | high | opus |  |
