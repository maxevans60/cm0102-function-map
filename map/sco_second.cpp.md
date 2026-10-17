# sco_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7f3250 | 156 (+2 unwind) | `ScoSecond::ScoSecond` | thiscall(ScoSecond* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Scottish Second Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x7f3460 | 11 | `ScoSecond::`scalar deleting destructor'` | thiscall(ScoSecond* this, unsigned flags) ret 4, returns this | Runs the ScoSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7f3480 | 60 (+1 unwind) | `ScoSecond::~ScoSecond` | thiscall(ScoSecond* this) ret 0 | Restores the Second Division vtable, frees the table, schedule and stage objects and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x7f3540 | 946 | `ScoSecond::create_schedule` | thiscall(ScoSecond* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 36-round schedule template of the Scottish Second Division for stage -1 and returns null otherwise. | high | opus |  |
| 0x7f3e80 | 84 | `ScoSecond::create_table` | thiscall(ScoSecond* this) ret 0, returns 1 on success and 0 on failure | Allocates the 10-row table and fills it with the clubs of the Scottish Second Division. | high | opus |  |
| 0x7f3f80 | 43 | `ScoSecond::set_up_rules` | thiscall(ScoSecond* this) ret 0, returns 1 | Sets the Second Division rule bytes, with the First Division above and the Third Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x7f4030 | 143 | `ScoSecond::start_new_season` | thiscall(ScoSecond* this) ret 0 | Frees last season's Second Division data, archives the stats, moves the year on and rebuilds the rules, table and fixtures. | high | opus |  |
