# spa_first.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x84e130 | 177 (+3 unwind) | `SpaFirst::SpaFirst` | thiscall(SpaFirst* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Spanish First Division on League, then loads saved data or sets up rules, table, fixtures and Comp_Stats, and creates the Spanish Lower Division. | high | opus | spa.md |
| 0x84e390 | 11 | `SpaFirst::`scalar deleting destructor'` | thiscall(SpaFirst* this, unsigned flags), returns this, ret 4 | Runs the SpaFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x84e3b0 | 44 (+1 unwind) | `SpaFirst::~SpaFirst` | thiscall(SpaFirst* this), ret 0 | Destroys the Spanish First Division, freeing its table, schedule and Comp_Stats and deleting the Spanish Lower Division object before the League destructor. | high | opus |  |
| 0x84e450 | 2563 | `SpaFirst::create_schedule` | thiscall(SpaFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 38-round schedule template of the Spanish First Division for stage -1, with even and odd year layouts, and returns null otherwise. | high | opus |  |
| 0x84fc70 | 124 | `SpaFirst::create_table` | thiscall(SpaFirst* this), returns 1 on success and 0 on failure, ret 0 | Moves Spanish Lower Division clubs to the generic lower division, fills the 20-row table with First Division clubs and pays the prize fund. | high | opus |  |
| 0x84fdf0 | 45 | `SpaFirst::set_up_rules` | thiscall(SpaFirst* this), returns 1, ret 0 | Sets the First Division rule bytes, with no league above and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x84feb0 | 161 | `SpaFirst::start_new_season` | thiscall(SpaFirst* this), ret 0 | Resolves B team clashes, runs Spanish promotion and relegation, exchanges lower clubs, rebuilds table and fixtures and restarts the lower leagues. | high | opus |  |
| 0x8500c0 | 195 | `SpaFirst::exchange_second_division_clubs_unplayed` | thiscall(SpaFirst* this), ret 0 | Without Segunda B, relegates Second Division clubs to group B1 and promotes as many from the Spanish Lower Division table or groups B1 to B4. | medium | opus |  |
| 0x850300 | 182 | `spa_first_exchange_second_division_b_clubs` | cdecl, no arguments, ret 0 | Moves relegated clubs of the four Segunda B groups to the generic lower division and promotes its best Spanish clubs in their place. | medium | opus |  |
| 0x850530 | 142 | `spa_first_assign_second_division_b_groups` | cdecl, no arguments, ret 0 | Sorts the 80 Segunda B clubs by stadium city latitude and longitude and assigns them by region to four groups of twenty. | high | opus |  |
| 0x850700 | 113 | `SpaFirst::process_promotion_relegation_chain` | thiscall(SpaFirst* this, int pairwise), ret 4 | Records final positions and swaps clubs between the First and Second Divisions, then between the Second Division and each loaded Segunda B group. | high | opus |  |
| 0x850880 | 23 | `SpaFirst::set_club_progress` | thiscall(SpaFirst* this, Club* club, int arg, char code1, char code2, char code3), ret 0x14 | Stores the three stage codes of a club in its Comp_Stats entry, with codes 17 and 18 mapped to 16 or 19. | high | opus |  |
| 0x8508c0 | 35 (+1 unwind) | `SpaFirst::load_extra_data` | thiscall(SpaFirst* this, File* file), returns 1, ret 4 | After a load, creates the Spanish Lower Division object at +0xee unless the nation flag shows that Segunda B is loaded. | high | opus | spa.md |
| 0x850950 | 7 | `SpaFirst::save_extra_data` | thiscall(SpaFirst* this, File* file), ret 4 | Writes the Spanish Lower Division object at +0xee to the save file through its save_to_temp_file slot when that object exists. | high | opus |  |
| 0x850970 | 506 | `SpaFirst::resolve_b_team_clashes` | thiscall(SpaFirst* this), ret 0 | Relegates or blocks B teams that would share a division with their senior club after the season, and hands the freed places to other clubs. | medium | opus |  |
