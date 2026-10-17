# hol_prm.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5f7610 | 156 (+2 unwind) | `HolPrm::HolPrm` | thiscall(HolPrm* this, short year, CompRecord* comp_record), returns this, ret 8 | Constructs the Dutch Premier Division on League, then loads saved data or builds rules, table, fixtures, Comp_Stats and predicted positions. | high | opus |  |
| 0x5f7820 | 11 | `HolPrm::`scalar deleting destructor'` | thiscall(HolPrm* this, unsigned flags), returns this, ret 4 | Runs the HolPrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5f7840 | 38 (+1 unwind) | `HolPrm::~HolPrm` | thiscall(HolPrm* this), ret 0 | Destroys the Dutch Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5f78d0 | 1240 | `HolPrm::create_schedule` | thiscall(HolPrm* this, char stage, short* round_count, short* comp_code, int* is_league), returns schedule template, ret 0x10 | Builds the 34-round schedule template of the Dutch Premier Division from mid-August for stage -1. | high | opus |  |
| 0x5f8430 | 99 | `HolPrm::create_table` | thiscall(HolPrm* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table, fills it with the Dutch Premier Division clubs, sets the prize fund from 50000 and pays the clubs. | high | opus |  |
| 0x5f8560 | 44 | `HolPrm::set_up_rules` | thiscall(HolPrm* this), returns 1, ret 0 | Sets the Premier Division rule bytes, with no league above and the First Division below, and builds the stage -1 schedule. | high | opus |  |
| 0x5f8610 | 142 | `HolPrm::start_new_season` | thiscall(HolPrm* this), ret 0 | Runs promotion and relegation, rebuilds the Premier Division table and fixtures, and starts the First Division season. | high | opus |  |
| 0x5f87e0 | 23 | `HolPrm::set_club_progress` | thiscall(HolPrm* this unused, Club* club, char stage unused, char code_a, char code_b, char code_c), ret 0x14 | Stores three progress codes in a club's Comp_Stats entry, mapping play-off codes 16 and 17 to 15 and 18. | high | opus |  |
