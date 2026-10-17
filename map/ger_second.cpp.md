# ger_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5de2e0 | 156 (+2 unwind) | `GerSecond::GerSecond` | thiscall(GerSecond* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the German Second Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x5de4f0 | 11 | `GerSecond::`scalar deleting destructor'` | thiscall(GerSecond* this, unsigned flags), returns this, ret 4 | Runs the GerSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5de510 | 60 (+1 unwind) | `GerSecond::~GerSecond` | thiscall(GerSecond* this), ret 0 | Destroys the German Second Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5de5d0 | 1402 | `GerSecond::create_schedule` | thiscall(GerSecond* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 34-round schedule template of the German Second Division from late July to May for stage -1 and returns null otherwise. | high | opus |  |
| 0x5df2b0 | 99 | `GerSecond::create_table` | thiscall(GerSecond* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table, fills it with the clubs of the German Second Division, sets the prize fund and pays each club 1300000. | high | opus |  |
| 0x5df3e0 | 45 | `GerSecond::set_up_rules` | thiscall(GerSecond* this), returns 1, ret 0 | Sets the German Second Division rule bytes, with the First Division above and an optional lower league, and builds the schedule for stage -1. | high | opus |  |
| 0x5df490 | 143 | `GerSecond::start_new_season` | thiscall(GerSecond* this), ret 0 | Clears the old season, archives statistics, moves the year on and rebuilds rules, table and fixtures, then reviews managers and officials. | high | opus |  |
