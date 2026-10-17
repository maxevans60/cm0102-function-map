# fra_third.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5bfb40 | 156 (+2 unwind) | `FraThird::FraThird` | thiscall(FraThird* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the French third division league, loads it from the temp file or sets up rules, table, fixtures and Comp_Stats, reporting errors by assert box. | high | opus |  |
| 0x5bfd50 | 11 | `FraThird::`scalar deleting destructor'` | thiscall(FraThird* this, unsigned flags), returns this, ret 4 | Destroys the French third division league and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x5bfd70 | 60 (+1 unwind) | `FraThird::~FraThird` | thiscall(FraThird* this), ret 0 | Restores the vtable, frees the table, schedule and stage objects and the Comp_Stats member, then runs the League base destructor. | high | opus |  |
| 0x5bfe30 | 816 | `FraThird::create_schedule` | thiscall(FraThird* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 38-round schedule of the French third division, setting each round's date and match slot from the season year. | high | opus |  |
| 0x5c05d0 | 99 | `FraThird::create_table` | thiscall(FraThird* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 20-row table, fills it with the clubs whose division is the French third division, sets the prize fund and pays each club. | high | opus |  |
| 0x5c0700 | 44 | `FraThird::set_up_rules` | thiscall(FraThird* this), returns 1, ret 0 | Sets the French third division rule bytes, with the Second Division above and no lower league, and builds the season schedule. | high | opus |  |
| 0x5c07c0 | 143 | `FraThird::start_new_season` | thiscall(FraThird* this), ret 0 | Frees the old table and stages, archives the stats, moves the year on, then rebuilds rules, table and fixtures for the new season. | high | opus |  |
