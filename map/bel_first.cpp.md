# bel_first.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x41dd40 | 158 (+2 unwind) | `BelFirst::BelFirst` | thiscall(BelFirst* this, short year, CompRecord* comp), ret 8 | Constructs the Belgian First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x41df60 | 11 | `BelFirst::`scalar deleting destructor'` | thiscall(BelFirst* this, unsigned flags), returns this, ret 4 | Runs the BelFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x41df80 | 38 (+1 unwind) | `BelFirst::~BelFirst` | thiscall(BelFirst* this), ret 0 | Destroys the Belgian First Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x41e010 | 929 | `BelFirst::create_schedule` | thiscall(BelFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 34-round schedule template of the Belgian First Division from mid August to May for stage -1 and returns null otherwise. | high | opus |  |
| 0x41e8b0 | 99 | `BelFirst::create_table` | thiscall(BelFirst* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table, fills it with the clubs of the Belgian First Division, sets the prize fund and pays each club 50000. | high | opus |  |
| 0x41e9e0 | 38 | `BelFirst::set_up_rules` | thiscall(BelFirst* this), returns 1, ret 0 | Sets the Belgian First Division rule bytes, with no upper league and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x41ea90 | 157 | `BelFirst::start_new_season` | thiscall(BelFirst* this), ret 0 | Runs promotion and relegation for all Belgian divisions, regroups the Third Division, then rebuilds table and fixtures and restarts the lower leagues. | high | opus |  |
| 0x41ec90 | 165 | `bel_first_move_third_division_clubs` | cdecl(void) ret 0 | Moves the play-off winners and four stored clubs into the Belgian Third Division and relegates its bottom clubs to Fourth Divisions A and B. | high | opus | hol-bel.md |
| 0x41ee80 | 67 | `BelFirst::process_promotion_relegation_chain` | thiscall(BelFirst* this, int pairwise unused), ret 4 | Records final positions in all Belgian divisions, then swaps clubs between First and Second and between Second and both Third Division groups. | high | opus |  |
| 0x41ef70 | 68 | `bel_first_split_third_division_groups` | cdecl(void) ret 0 | Sorts the 32 Belgian Third Division clubs by longitude and puts the first 16 in Third Division A and the rest in Third Division B. | high | opus |  |
