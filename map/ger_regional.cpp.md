# ger_regional.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5dcbd0 | 162 (+2 unwind) | `GerRegional::GerRegional` | thiscall(GerRegional* this, short year, CompRecord* comp), returns this, ret 8 | Constructs German Regional on League, then sets up rules, the North table, Comp_Stats, fixtures, the South stage and predicted positions. | high | opus |  |
| 0x5dce00 | 2 | `shared_return_false` | thiscall(void* this) ret 0, returns 0 | Returns zero for Comp slots 30 get_finals_comp and 34, and for the has_relegation slot of GerRegional. | high | opus |  |
| 0x5dce10 | 11 | `GerRegional::`scalar deleting destructor'` | thiscall(GerRegional* this, unsigned flags), returns this, ret 4 | Runs the GerRegional destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5dce30 | 60 (+1 unwind) | `GerRegional::~GerRegional` | thiscall(GerRegional* this), ret 0 | Destroys German Regional, freeing its table, schedule, child stages and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5dcef0 | 992 | `GerRegional::create_schedule` | thiscall(GerRegional* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 34-round schedule template of German Regional, or 38 rounds for stage -1 in 2000, with dates and match slots. | high | opus |  |
| 0x5dd7f0 | 154 | `GerRegional::create_table` | thiscall(GerRegional* this), returns bool, ret 0 | Allocates the North table of 18 rows, or 19 in 2000, and fills it with Regional clubs of the North section. | high | opus |  |
| 0x5dd9f0 | 37 | `GerRegional::set_up_rules` | thiscall(GerRegional* this), returns 1, ret 0 | Sets the Regional rule bytes, with the Second Division above and no league below, and builds the schedule for stage -1. | high | opus |  |
| 0x5dda90 | 144 | `GerRegional::start_new_season` | thiscall(GerRegional* this), ret 0 | Frees the table and child stages, archives the stats, advances the year and rebuilds rules, North table, fixtures and South stage. | high | opus |  |
| 0x5ddc50 | 269 (+1 unwind) | `GerRegional::create_south_stage` | thiscall(GerRegional* this, int stage), ret 4 | Collects the 18 Regional clubs of the South section and builds them into a League_Stage stored as the child stage. | high | opus |  |
| 0x5ddff0 | 95 | `GerRegional::get_club_array` | thiscall(GerRegional* this, Club*** out_clubs, short* out_count), ret 8 | Allocates an array of the clubs of the North table followed by the South stage and returns it with the count. | high | opus |  |
| 0x5de130 | 122 | `GerRegional::set_predicted_positions` | thiscall(GerRegional* this), ret 0 | Sorts the clubs of each Regional section by reputation and stores interleaved odd predicted positions in the stats. | high | opus |  |
| 0x5de2a0 | 17 | `GerRegional::set_club_progress` | thiscall(GerRegional* this, Club* club, int arg, char code1, char code2, char code3), ret 0x14 | Stores the three stage codes of a club in its Comp_Stats entry as odd values, mapping each code c to 2c minus 1. | high | opus |  |
