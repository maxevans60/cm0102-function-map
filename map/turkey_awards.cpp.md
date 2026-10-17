# turkey_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x901c70 | 40 (+1 unwind) | `TurkeyAwards::TurkeyAwards` | thiscall(TurkeyAwards* this, FILE* source) ret 4, returns this | Builds the Turkish awards object on NationAwards, then loads the awards from the file or creates them. | high | opus |  |
| 0x901d00 | 219 (+6 unwind) | `TurkeyAwards::init_awards` | thiscall(TurkeyAwards* this, FILE* source) ret 4 | Creates the six Turkish awards, two year awards and four divisional team awards for the two leagues. | high | opus |  |
| 0x901fd0 | 64 | `TurkeyAwards::daily_update` | thiscall(TurkeyAwards* this, Date* date) ret 4 | On 30 May, gives the Turkish player of the year, manager of the year and team of the season awards, then runs the base update. | high | opus |  |
| 0x902080 | 12 | `TurkeyAwards::update_team_of_the_week` | thiscall(TurkeyAwards* this, void* award) ret 4 | Builds the team of the week for an award when it is one of the two Turkish divisional team awards. | high | opus |  |
