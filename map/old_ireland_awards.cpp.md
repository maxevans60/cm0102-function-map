# old_ireland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x79ea00 | 82 (+2 unwind) | `OldIrelandAwards::OldIrelandAwards` | thiscall(OldIrelandAwards* this, FILE* file or 0) ret 4, returns this | Constructs the old Irish awards on NationAwards, sets the nation record, then loads saved awards or creates the month ratings and award table. | high | opus |  |
| 0x79eb40 | 547 (+17 unwind) | `OldIrelandAwards::init_awards` | thiscall(OldIrelandAwards* this, FILE* file or 0) ret 4 | Allocates the table of seventeen old Irish awards and creates the year, month and team awards of the nation and both divisions. | high | opus |  |
| 0x79f250 | 219 | `OldIrelandAwards::daily_update` | thiscall(OldIrelandAwards* this, Date* date) ret 4 | Gives the old Irish year awards of the nation and both divisions on 1 May, moves the month award slots, then runs the base update. | high | opus |  |
| 0x79f490 | 42 | `OldIrelandAwards::on_month_change` | thiscall(OldIrelandAwards* this) ret 0, this unused | Gives the manager of the month award of each Irish division to the best staff record of that division. | high | opus |  |
| 0x79f510 | 12 | `OldIrelandAwards::update_team_of_the_week` | thiscall(OldIrelandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is the team award of either Irish division. | high | opus |  |
