# brazil_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x43d2b0 | 40 (+1 unwind) | `BrazilAwards::BrazilAwards` | thiscall(BrazilAwards* this, FILE* file) ret 4, returns this | Constructs the Brazilian awards on NationAwards and loads them from the file, or sets them up fresh when loading fails. | high | opus |  |
| 0x43d340 | 1717 (+58 unwind) | `BrazilAwards::init_awards` | thiscall(BrazilAwards* this, FILE* file) ret 4 | Creates the 58 Brazilian awards, team and yearly awards for both national divisions and for the twelve state championships. | high | opus |  |
| 0x43e990 | 688 | `BrazilAwards::daily_update` | thiscall(BrazilAwards* this, Date* date) ret 4 | Gives the state championship player awards on one fixed date and the national division awards on another, then runs the base month change check. | high | opus |  |
| 0x43f070 | 36 | `BrazilAwards::update_team_of_the_week` | thiscall(BrazilAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is one of the 14 weekly team awards in the Brazilian award table. | high | opus |  |
