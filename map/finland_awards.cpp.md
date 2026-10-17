# finland_awards.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5a8f70 | 82 (+2 unwind) | `FinlandAwards::FinlandAwards` | thiscall(FinlandAwards *this, int save_file: 0 for a new game) ret 4 | Constructs the Finland awards object, loading it from the save or creating the month ratings and award table. | high | opus |  |
| 0x5a90b0 | 464 (+14 unwind) | `FinlandAwards::init_awards` | thiscall(FinlandAwards *this, int owner) ret 4 | Allocates the table of fourteen Finland award objects for year, month and team awards. | high | opus | 2026-10-14-widescreen-inventory.md |
| 0x5a96b0 | 19 | `FinlandAwards::record_match_ratings` | thiscall(FinlandAwards* this, Fixture* fixture, MatchResult* result) ret 8 | Passes a played match to the month ratings when its competition is a league division. | high | opus |  |
| 0x5a96e0 | 160 | `FinlandAwards::daily_update` | thiscall(FinlandAwards *this, Date *today) ret 4 | Gives the Finland season awards on 15 October, advances the month award slots at season start and runs the base daily update. | high | opus |  |
| 0x5a9890 | 54 | `FinlandAwards::on_month_change` | thiscall(FinlandAwards *this) ret 0 | Gives the monthly awards for the two Finnish league competitions and closes the month award entries. | high | opus |  |
| 0x5a9930 | 12 | `FinlandAwards::update_team_of_the_week` | thiscall(FinlandAwards *this, Award *award) ret 4 | Builds the team of the week when the award is one of the two Finnish team awards. | high | opus |  |
