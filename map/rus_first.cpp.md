# rus_first.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e9f30 | 156 (+2 unwind) | `RusFirst::RusFirst` | thiscall(RusFirst* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Russian First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x7ea140 | 11 | `RusFirst::`scalar deleting destructor'` | thiscall(RusFirst* this, unsigned flags), returns this, ret 4 | Runs the Russian First Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ea160 | 57 (+1 unwind) | `RusFirst::~RusFirst` | thiscall(RusFirst* this), ret 0 | Destroys the Russian First Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7ea220 | 483 | `RusFirst::create_schedule` | thiscall(RusFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 36-round schedule template of the Russian First Division from month index 3 to 10 for stage -1 and returns null otherwise. | high | opus |  |
| 0x7ea6c0 | 111 | `RusFirst::create_table` | thiscall(RusFirst* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table, picks the 18 strongest First Division clubs and moves any surplus clubs down to the Second Division zone 0x9cf91c. | high | opus |  |
| 0x7ea810 | 43 | `RusFirst::set_up_rules` | thiscall(RusFirst* this), returns 1, ret 0 | Sets the Russian First Division rule bytes, with the Premier League above and no lower league, and builds the schedule for stage -1. | high | opus |  |
| 0x7ea8c0 | 143 | `RusFirst::start_new_season` | thiscall(RusFirst* this), ret 0 | Frees the table, schedule and stages, archives the season, moves the year on and rebuilds rules, table and fixtures for the Russian First Division. | high | opus |  |
