# cro_a1.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x513e10 | 158 (+2 unwind) | `CroA1::CroA1` | thiscall(CroA1* this, short year, CompRecord* comp), ret 8 | Constructs the Croatian First Division on League, then loads saved data or sets up rules, table, fixtures, sort order and Comp_Stats. | high | opus |  |
| 0x514030 | 11 | `CroA1::`scalar deleting destructor'` | thiscall(CroA1* this, unsigned flags), returns this, ret 4 | Destroys the Croatian First Division object and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x514050 | 38 (+1 unwind) | `CroA1::~CroA1` | thiscall(CroA1* this), ret 0 | Destroys the Croatian First Division, freeing its table, schedule at +0xba and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5140e0 | 739 | `CroA1::create_schedule` | thiscall(CroA1* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 30-round league schedule from late July to May for stage -1, or the one-round play-off of tied clubs in May for stage 0. | high | opus |  |
| 0x5147b0 | 99 | `CroA1::create_table` | thiscall(CroA1* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 16-row table, fills it with the clubs of the Croatian First Division, sets the prize fund and pays each club 100000. | high | opus |  |
| 0x5148e0 | 46 | `CroA1::set_up_rules` | thiscall(CroA1* this), returns int, ret 0 | Sets the Croatian league rules, with the second division group of 0x9cf8a8 as the lower league, and builds the schedule for stage -1. | high | opus |  |
| 0x5149a0 | 169 | `CroA1::start_new_season` | thiscall(CroA1* this), ret 0 | Promotes and relegates clubs, realigns the second division groups, clears the old season and rebuilds rules, table and fixtures for the new year. | high | opus |  |
| 0x514bd0 | 40 | `CroA1::advance_stage` | thiscall(CroA1* this), ret 0 | Moves the current stage index at +0x30 on by one and creates the play-off stage when it reaches stage 0. | high | opus |  |
| 0x514c60 | 192 (+1 unwind) | `CroA1::create_playoff_stage` | thiscall(CroA1* this), ret 0 | Pairs adjacent table clubs level on points into a play-off Cup_Stage, or ends the competition when no clubs tie. | medium | opus |  |
| 0x514ed0 | 175 | `cro_a1_swap_second_and_third_tier_clubs` | cdecl(void), ret 0 | Promotes four top Croatian lower tier clubs into the second division and moves its relegated clubs down to the third tier. | medium | opus |  |
| 0x5150f0 | 45 | `CroA1::process_promotion_relegation_chain` | thiscall(CroA1* this, int pairwise unused), ret 4 | Records final positions in the first division and both second division groups, then swaps clubs between the first division and each group. | high | opus |  |
| 0x515190 | 105 (+1 unwind) | `cro_a1_realign_second_division_groups` | cdecl(void) ret 0 | Sorts the 32 second division clubs by the latitude of their stadium city, puts the first 16 in group 0x9cf8a8 and the rest in 0x9cf8ac, and tells human managers. | medium | opus |  |
| 0x5152f0 | 10 | `CroA1::load_extra_data` | thiscall(CroA1* this, FILE* file), returns 1, ret 4 | Reads the one-byte play-off pair count at +0xee from the saved game file. | high | opus |  |
