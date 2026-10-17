# japan_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x666690 | 40 (+1 unwind) | `JapanAwards::JapanAwards` | thiscall(JapanAwards* this, FILE* file) ret 4, returns this | Builds the Japan awards object, loads it from a save file when one is given, or creates its award objects. | high | opus |  |
| 0x666720 | 275 (+8 unwind) | `JapanAwards::init_awards` | thiscall(JapanAwards* this, FILE* file) ret 4 | Allocates the eight-award table and builds four year awards and four team awards for the J1 and J2 Leagues. | high | opus |  |
| 0x666ab0 | 95 | `JapanAwards::daily_update` | thiscall(JapanAwards* this, Date* date) ret 4 | On 20 December gives the J1 year awards and the J1 and J2 team awards, then checks for a month change. | high | opus |  |
| 0x666bb0 | 12 | `JapanAwards::update_team_of_the_week` | thiscall(JapanAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the award is the J1 or the J2 weekly team award. | high | opus |  |
