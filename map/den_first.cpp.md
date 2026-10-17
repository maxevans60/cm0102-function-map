# den_first.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5516f0 | 156 (+2 unwind) | `DenFirst::DenFirst` | thiscall(DenFirst* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Danish First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and stats. | high | opus |  |
| 0x551900 | 11 | `DenFirst::`scalar deleting destructor'` | thiscall(DenFirst* this, unsigned flags) ret 4, returns this | Runs the Danish First Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x551920 | 38 (+1 unwind) | `DenFirst::~DenFirst` | thiscall(DenFirst* this) ret 0 | Destroys the Danish First Division, freeing its table, schedule and stats before the League destructor runs. | high | opus |  |
| 0x5519b0 | 949 | `DenFirst::create_schedule` | thiscall(DenFirst* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 30-round schedule template of the Danish First Division from early August, with spring dates set by year parity, for stage -1. | high | opus |  |
| 0x552290 | 95 | `DenFirst::create_table` | thiscall(DenFirst* this) ret 0, returns 1 on success and 0 on failure | Allocates the 16-row table, fills it with the clubs of the Danish First Division and sets the prize fund. | high | opus |  |
| 0x5523b0 | 38 | `DenFirst::set_up_rules` | thiscall(DenFirst* this) ret 0, returns 1 | Sets the Danish First Division rule bytes, with the Premier Division above and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x552450 | 125 | `DenFirst::start_new_season` | thiscall(DenFirst* this) ret 0 | Frees last season's table and schedule, archives stats, advances the year and rebuilds rules, table, fixtures and predicted positions. | high | opus |  |
