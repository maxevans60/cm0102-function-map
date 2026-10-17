# usa_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x906980 | 82 (+2 unwind) | `UsaAwards::UsaAwards` | thiscall(UsaAwards* this, FILE* source) ret 4, returns this | Builds the USA awards object on NationAwards with month ratings, then loads the awards from the file or creates them. | high | opus |  |
| 0x906ac0 | 257 (+7 unwind) | `UsaAwards::init_awards` | thiscall(UsaAwards* this, FILE* source) ret 4 | Creates the seven USA awards, a month award, five year awards and a team award for the MLS. | high | opus |  |
| 0x906e10 | 122 | `UsaAwards::daily_update` | thiscall(UsaAwards* this, Date* date) ret 4 | On 25 November, gives the MLS manager, player and team of the season awards, advances the month award slots, then runs the base update. | high | opus |  |
| 0x906f60 | 7 | `UsaAwards::on_month_change` | thiscall(UsaAwards* this) ret 0 | Gives the USA player of the month award from the month ratings. | high | opus |  |
