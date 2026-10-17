# por_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7d0950 | 156 (+2 unwind) | `PorSecond::PorSecond` | thiscall(PorSecond* this, short year, CompRecord* comp) ret 8, returns this | Builds the Portuguese Second Division on League, loads it from the temp file or sets rules, table, fixtures and statistics. | high | opus |  |
| 0x7d0b60 | 11 | `PorSecond::`scalar deleting destructor'` | thiscall(PorSecond* this, unsigned flags) ret 4, returns this | Destroys the Portuguese Second Division and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x7d0b80 | 60 (+1 unwind) | `PorSecond::~PorSecond` | thiscall(PorSecond* this) ret 0 | Frees the table and schedule, deletes each stage and the stage array and the statistics object, then runs the League destructor. | high | opus |  |
| 0x7d0c40 | 961 | `PorSecond::create_schedule` | thiscall(PorSecond* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 34-round schedule template of the Second Division from late August, with one match slot on each round. | high | opus |  |
| 0x7d1520 | 122 | `PorSecond::create_table` | thiscall(PorSecond* this) ret 0, returns 1 on success and 0 on failure | Allocates the 18-row table, fills it with the Second Division clubs, marks B teams of Premier Division clubs and sets the prize fund. | high | opus |  |
| 0x7d16a0 | 46 | `PorSecond::set_up_rules` | thiscall(PorSecond* this) ret 0, returns 1 | Sets the Second Division rules with promotion to the Premier Division and relegation to Second Division B when it exists, then builds the schedule. | high | opus |  |
| 0x7d1760 | 143 | `PorSecond::start_new_season` | thiscall(PorSecond* this) ret 0 | Frees the table, schedule and stages, archives the statistics, adds one to the year and rebuilds rules, table and fixtures. | high | opus |  |
