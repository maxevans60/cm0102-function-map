# spa_lower.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x851020 | 107 (+1 unwind) | `SpaLower::SpaLower` | thiscall(SpaLower* this, short year), returns this, ret 4 | Constructs the Spanish Lower Division on League for comp 0x9cf6b0, then loads saved data or sets up rules, table and fixtures. | high | opus | spa.md |
| 0x851190 | 11 | `SpaLower::`scalar deleting destructor'` | thiscall(SpaLower* this, unsigned flags), returns this, ret 4 | Runs the SpaLower destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x8511b0 | 52 (+1 unwind) | `SpaLower::~SpaLower` | thiscall(SpaLower* this), ret 0 | Destroys the Spanish Lower Division, freeing its table, schedule and stage objects before the League destructor runs. | high | opus |  |
| 0x851260 | 3606 | `SpaLower::create_schedule` | thiscall(SpaLower* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 42-round schedule template of the Spanish Lower Division for stage -1, with layouts for even and odd years, and returns null otherwise. | high | opus |  |
| 0x8533d0 | 301 | `SpaLower::create_table` | thiscall(SpaLower* this), returns true when all 22 rows are filled, ret 0 | Fills the 22-row table with B teams of First and then Second Division clubs, then with the best other Spanish lower clubs by reputation. | high | opus |  |
| 0x853790 | 36 | `SpaLower::set_up_rules` | thiscall(SpaLower* this), returns 1, ret 0 | Sets the Spanish Lower Division rule bytes, with the First Division as the league above and none below, and builds the schedule for stage -1. | high | opus |  |
| 0x853830 | 119 | `SpaLower::start_new_season` | thiscall(SpaLower* this), ret 0 | Archives the season, frees the table, schedule and stage objects, then sets up rules, refills the table and builds new fixtures. | high | opus |  |
