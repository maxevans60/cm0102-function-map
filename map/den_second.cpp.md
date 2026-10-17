# den_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x553e80 | 156 (+2 unwind) | `DenSecond::DenSecond` | thiscall(DenSecond* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Danish Second Division on League, loads it from the temp file or builds rules, table, fixtures and Comp_Stats, reporting failed steps. | high | opus |  |
| 0x554090 | 11 | `DenSecond::`scalar deleting destructor'` | thiscall(DenSecond* this, unsigned flags) ret 4, returns this | Runs the DenSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5540b0 | 57 (+1 unwind) | `DenSecond::~DenSecond` | thiscall(DenSecond* this) ret 0 | Destroys the Danish Second Division, freeing its table, schedule, every stage object and Comp_Stats before the League base destructor. | high | opus |  |
| 0x554170 | 945 | `DenSecond::create_schedule` | thiscall(DenSecond* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 30-round schedule of the Danish Second Division from August, with different spring dates in odd and even years. | high | opus |  |
| 0x554a40 | 95 | `DenSecond::create_table` | thiscall(DenSecond* this) ret 0, returns 1 on success and 0 on failure | Allocates the 16-row table, fills it with the clubs of the Danish Second Division and sets the prize fund. | high | opus |  |
| 0x554b60 | 40 | `DenSecond::set_up_rules` | thiscall(DenSecond* this) ret 0, returns 1 | Sets the Danish Second Division rules with the First Division above and no division below, then builds the schedule through the virtual call. | high | opus |  |
| 0x554c00 | 143 | `DenSecond::start_new_season` | thiscall(DenSecond* this) ret 0 | Frees the old table, schedule and stages, archives Comp_Stats, increments the year and rebuilds rules, table, fixtures and sorted table. | high | opus |  |
