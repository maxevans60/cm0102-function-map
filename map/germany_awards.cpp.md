# germany_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5df650 | 82 (+2 unwind) | `GermanyAwards::GermanyAwards` | thiscall(GermanyAwards* this, FILE* file or 0), returns this, ret 4 | Constructs the German awards on NationAwards and loads them from the file, or creates the month ratings and sets up the awards fresh. | high | opus |  |
| 0x5df790 | 459 (+14 unwind) | `GermanyAwards::init_awards` | thiscall(GermanyAwards* this, FILE* file or 0), ret 4 | Allocates the fourteen-entry award table and constructs the German year, team and month awards for the two Bundesliga divisions. | high | opus |  |
| 0x5dfd70 | 182 | `GermanyAwards::daily_update` | thiscall(GermanyAwards* this, Date* date), ret 4 | On 6 June gives the German yearly player and manager awards, moves the month award slots at season end, then runs the base month check. | high | opus |  |
| 0x5dff40 | 16 | `GermanyAwards::on_month_change` | thiscall(GermanyAwards* this), ret 0 | Gives the German player of the month awards from the month ratings, once for all players and once for the age limit of 20. | high | opus |  |
