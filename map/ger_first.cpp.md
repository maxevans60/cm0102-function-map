# ger_first.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5d99b0 | 156 (+2 unwind) | `GerFirst::GerFirst` | thiscall(GerFirst* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the German First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table, Comp_Stats and predicted positions. | high | opus |  |
| 0x5d9bc0 | 11 | `GerFirst::`scalar deleting destructor'` | thiscall(GerFirst* this, unsigned flags), returns this, ret 4 | Runs the GerFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5d9be0 | 38 (+1 unwind) | `GerFirst::~GerFirst` | thiscall(GerFirst* this), ret 0 | Destroys the German First Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5d9c70 | 2395 | `GerFirst::create_schedule` | thiscall(GerFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 34-round schedule template of the German First Division for stage -1 with round dates and match slots. | high | opus |  |
| 0x5db230 | 147 | `GerFirst::create_table` | thiscall(GerFirst* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table and fills it with First Division clubs, and in 2001 moves clubs of the four regional divisions into German Regional. | high | opus |  |
| 0x5db400 | 40 | `GerFirst::set_up_rules` | thiscall(GerFirst* this), returns 1, ret 0 | Sets the First Division rule bytes, with no upper league and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x5db4a0 | 167 | `GerFirst::start_new_season` | thiscall(GerFirst* this), ret 0 | Runs promotion and relegation for the German pyramid, exchanges Regional clubs, rebuilds table and fixtures and restarts the Second Division and Regional. | high | opus |  |
| 0x5db6c0 | 69 | `GerFirst::process_promotion_relegation_chain` | thiscall(GerFirst* this, int pairwise), ret 4 | Records final positions and swaps clubs between the First and Second Divisions, then between the Second Division and both Regional sections. | high | opus |  |
| 0x5db7b0 | 161 | `ger_first_exchange_regional_clubs_unplayed` | cdecl, no arguments, ret 0 | When German Regional is not played, promotes the four strongest eligible Regional clubs to the Second Division and moves relegated Second Division clubs down. | high | opus |  |
| 0x5db980 | 187 | `ger_first_exchange_regional_lower_division_clubs` | cdecl, no arguments, ret 0 | Moves relegated clubs of both Regional sections to the lower division and promotes the same number of German lower division clubs into German Regional. | high | opus |  |
| 0x5dbbd0 | 299 | `ger_first_split_regional_north_south` | cdecl, no arguments, ret 0 | Splits the 36 German Regional clubs into North and South groups of 18 by city latitude, keeping clubs in their old section where possible. | medium | opus |  |
| 0x5dbf50 | 114 | `ger_first_relegate_b_teams_of_relegated_clubs` | cdecl, no arguments, ret 0 | Marks a Regional B team as relegated when its senior club drops from the Second Division, and posts the override news. | high | opus |  |
