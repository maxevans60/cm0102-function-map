# northern_ireland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x792d80 | 82 (+2 unwind) | `NorthernIrelandAwards::NorthernIrelandAwards` | thiscall(NorthernIrelandAwards* this, FILE* file) ret 4, returns this | Constructs the Northern Ireland awards on NationAwards, sets its nation, then loads saved awards or creates month ratings and the award table. | high | opus |  |
| 0x792ec0 | 435 (+13 unwind) | `NorthernIrelandAwards::init_awards` | thiscall(NorthernIrelandAwards* this, FILE* file) ret 4 | Allocates the table of thirteen awards: one national year award, and for each of two divisions a team award, four year awards and a month award. | high | opus |  |
| 0x793460 | 175 | `NorthernIrelandAwards::daily_update` | thiscall(NorthernIrelandAwards* this, Date* date) ret 4 | On 20 May gives the national and divisional player, young player and manager of the year awards, advances month slots, then runs the base update. | high | opus |  |
| 0x793630 | 42 | `NorthernIrelandAwards::on_month_change` | thiscall(NorthernIrelandAwards* this) ret 0 | Gives the manager of the month award of each of the two Northern Ireland divisions from the best staff record of the month. | high | opus |  |
| 0x7936b0 | 12 | `NorthernIrelandAwards::update_team_of_the_week` | thiscall(NorthernIrelandAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is one of the two Northern Ireland divisional team awards. | high | opus |  |
