# ireland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63b640 | 88 (+2 unwind) | `IrelandAwards::IrelandAwards` | thiscall(IrelandAwards* this, FILE* file or 0) ret 4, returns this | Constructs the Irish awards on NationAwards, sets the nation record, then loads saved awards or creates the month ratings and award table. | high | opus |  |
| 0x63b790 | 579 (+18 unwind) | `IrelandAwards::init_awards` | thiscall(IrelandAwards* this, FILE* file or 0) ret 4 | Allocates the table of eighteen Irish awards and creates the year, month and team awards of the nation and both divisions. | high | opus |  |
| 0x63bf10 | 224 | `IrelandAwards::daily_update` | thiscall(IrelandAwards* this, Date* date) ret 4 | Gives the Irish year awards of the nation and both divisions on 1 May, moves the month award slots, then runs the base update. | high | opus |  |
| 0x63c160 | 48 | `IrelandAwards::on_month_change` | thiscall(IrelandAwards* this) ret 0 | Gives the player of the month award, then the manager of the month awards of both divisions to their best staff records. | high | opus |  |
| 0x63c1f0 | 12 | `IrelandAwards::update_team_of_the_week` | thiscall(IrelandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is the team award of the Premier or First Division. | high | opus |  |
