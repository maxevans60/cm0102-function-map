# old_finland_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x79d540 | 82 (+2 unwind) | `OldFinlandAwards::OldFinlandAwards` | thiscall(OldFinlandAwards* this, FILE* save) ret 4, returns this | Constructs the old-format Finland awards object, then loads saved awards or creates the month ratings and award table. | high | opus |  |
| 0x79d680 | 366 (+11 unwind) | `OldFinlandAwards::init_awards` | thiscall(OldFinlandAwards* this, FILE* save) ret 4 | Allocates the table of eleven old Finland awards with year, month and team awards for the two Finnish leagues. | high | opus | 2026-10-14-widescreen-inventory.md |
| 0x79db30 | 141 | `OldFinlandAwards::daily_update` | thiscall(OldFinlandAwards* this, Date* today) ret 4 | Gives the old Finland season awards on 15 October, advances the month award slots at season start and runs the base daily update. | high | opus |  |
| 0x79dcb0 | 7 | `OldFinlandAwards::on_month_change` | thiscall(OldFinlandAwards* this) ret 0 | Gives the monthly player award from the month ratings when the month changes. | high | opus |  |
| 0x79dcd0 | 12 | `OldFinlandAwards::update_team_of_the_week` | thiscall(OldFinlandAwards* this, TeamAward* award) ret 4 | Builds the team of the week when the given award is one of the two old Finland team awards. | high | opus |  |
