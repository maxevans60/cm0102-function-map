# italy_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x65fe30 | 40 (+1 unwind) | `ItalyAwards::ItalyAwards` | thiscall(ItalyAwards* this, FILE* file) ret 4, returns this | Builds the Italian awards object, loads it from a save file when one is given, or creates its award objects. | high | opus |  |
| 0x65fec0 | 1223 (+40 unwind) | `ItalyAwards::init_awards` | thiscall(ItalyAwards* this, FILE* file) ret 4 | Allocates the award table and constructs the yearly, monthly and team awards of each Italian division, adding the lower divisions when they exist. | high | opus |  |
| 0x660ec0 | 429 | `ItalyAwards::daily_update` | thiscall(ItalyAwards* this, Date* date) ret 4 | Gives the yearly manager, player and team awards of each Italian division on a fixed date, then runs the base daily update. | high | opus |  |
| 0x661330 | 27 | `ItalyAwards::update_team_of_the_week` | thiscall(ItalyAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week nominations when the given award is the team award of one of the Italian divisions. | high | opus |  |
