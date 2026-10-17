# sco_third.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7f41f0 | 156 (+2 unwind) | `ScoThird::ScoThird` | thiscall(ScoThird* this, short year, club_comp* comp) ret 8, returns this | Constructs the Scottish Third Division on the League base, loads it from the temp file or sets up its rules, table, fixtures and stats. | high | opus |  |
| 0x7f4400 | 11 | `ScoThird::`scalar deleting destructor'` | thiscall(ScoThird* this, unsigned flags) ret 4, returns this | Runs the Third Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7f4420 | 60 (+1 unwind) | `ScoThird::~ScoThird` | thiscall(ScoThird* this) ret 0 | Destroys the Third Division by freeing its table, schedule, stage objects and stats, then runs the League destructor. | high | opus |  |
| 0x7f44e0 | 946 | `ScoThird::create_schedule` | thiscall(ScoThird* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 36-matchday league schedule for stage -1 and returns null for any other stage. | high | opus |  |
| 0x7f4e20 | 84 | `ScoThird::create_table` | thiscall(ScoThird* this) ret 0, returns 1 on success | Allocates the 10-row league table and fills it with the clubs of the Scottish Third Division. | high | opus |  |
| 0x7f4f20 | 36 | `ScoThird::set_up_rules` | thiscall(ScoThird* this) ret 0, returns 1 | Sets the Third Division rules with two promoted clubs and no relegation, then builds the league schedule. | high | opus |  |
| 0x7f4fb0 | 143 | `ScoThird::start_new_season` | thiscall(ScoThird* this) ret 0 | Clears the old season, archives the stats, moves the year on and rebuilds the rules, table, fixtures and predicted positions. | high | opus |  |
