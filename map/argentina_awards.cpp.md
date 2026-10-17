# argentina_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x40a350 | 40 (+1 unwind) | `ArgentinaAwards::ArgentinaAwards` | thiscall(ArgentinaAwards* this, void* file) ret 4 | Constructs the Argentine awards on NationAwards and loads them from the file, or sets them up fresh when loading fails. | high | opus |  |
| 0x40a3e0 | 107 (+2 unwind) | `ArgentinaAwards::init_awards` | thiscall(ArgentinaAwards* this, void* file) ret 4 | Creates the two team awards, one for the first division and one for the second division. | high | opus |  |
| 0x40a550 | 4 | `ArgentinaAwards::daily_update` | thiscall(ArgentinaAwards* this, int date) ret 4 | Forwards the daily update to the NationAwards base month change check. | high | opus |  |
| 0x40a560 | 12 | `ArgentinaAwards::update_team_of_the_week` | thiscall(ArgentinaAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week when the given award is one of the two Argentine team awards. | high | opus |  |
