# fra_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5be330 | 156 (+2 unwind) | `FraSecond::FraSecond` | thiscall(FraSecond* this, short year, void* comp_record), ret 8 | Constructs the French Second Division on League, loads it from the temp file or sets rules, fills the table, builds fixtures, stats and predictions. | high | opus |  |
| 0x5be540 | 11 | `FraSecond::`scalar deleting destructor'` | thiscall(FraSecond* this, unsigned flags), ret 4, returns this | Runs the French Second Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5be560 | 60 (+1 unwind) | `FraSecond::~FraSecond` | thiscall(FraSecond* this), ret 0 | Destroys the French Second Division by freeing its table, schedule, stage objects and stats, then runs the League destructor. | high | opus |  |
| 0x5be620 | 961 | `FraSecond::create_schedule` | thiscall(FraSecond* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 38-round schedule template of the French Second Division from late July to late May for stage -1 and returns null otherwise. | high | opus |  |
| 0x5bef10 | 127 | `FraSecond::create_table` | thiscall(FraSecond* this), ret 0, returns 1 or 0 | Allocates the 20-row table, fills it with the Second Division clubs and pays each club a grant by its previous division. | high | opus |  |
| 0x5bf0a0 | 45 | `FraSecond::set_up_rules` | thiscall(FraSecond* this), returns 1, ret 0 | Sets the French Second Division rules with the First Division above and the third division below, and builds the schedule for stage -1. | high | opus |  |
| 0x5bf160 | 143 | `FraSecond::start_new_season` | thiscall(FraSecond* this), ret 0 | Frees the old table, schedule and stages, archives the stats, increments the year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
