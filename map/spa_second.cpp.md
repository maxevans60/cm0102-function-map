# spa_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8539a0 | 156 (+2 unwind) | `SpaSecond::SpaSecond` | thiscall(SpaSecond* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Spanish Second Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x853bb0 | 11 | `SpaSecond::`scalar deleting destructor'` | thiscall(SpaSecond* this, unsigned flags), returns this, ret 4 | Runs the SpaSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x853bd0 | 60 (+1 unwind) | `SpaSecond::~SpaSecond` | thiscall(SpaSecond* this), ret 0 | Destroys the Spanish Second Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x853c90 | 3350 | `SpaSecond::create_schedule` | thiscall(SpaSecond* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 42-round schedule template of the Spanish Second Division for stage -1, with layouts for even and odd years, and returns null otherwise. | high | opus |  |
| 0x855b40 | 122 | `SpaSecond::create_table` | thiscall(SpaSecond* this), returns 1 on success and 0 on failure, ret 0 | Fills the 22-row table with Second Division clubs, marks B teams of First Division clubs as barred from promotion and sets the prize fund. | high | opus |  |
| 0x855cc0 | 47 | `SpaSecond::set_up_rules` | thiscall(SpaSecond* this), returns 1, ret 0 | Sets the Second Division rule bytes, with the First Division above and Segunda B below when loaded, and builds the schedule for stage -1. | high | opus | spa.md |
| 0x855d80 | 143 | `SpaSecond::start_new_season` | thiscall(SpaSecond* this), ret 0 | Archives the season, frees the table, schedule and stage objects, then sets up rules, refills and sorts the table, builds fixtures and reviews managers. | high | opus |  |
