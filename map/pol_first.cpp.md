# pol_first.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7c8a80 | 203 (+2 unwind) | `PolFirst::PolFirst` | thiscall(PolFirst* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Polish First Division, then loads saved data or sets up rules, the first group table, fixtures, stats and the second group. | high | opus |  |
| 0x7c8d30 | 11 | `PolFirst::`scalar deleting destructor'` | thiscall(PolFirst* this, unsigned flags) ret 4, returns this | Runs the Polish First Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7c8d50 | 44 (+1 unwind) | `PolFirst::~PolFirst` | thiscall(PolFirst* this) ret 0 | Destroys the Polish First Division, freeing its table, club slot list, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7c8df0 | 653 | `PolFirst::create_schedule` | thiscall(PolFirst* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds a 14-round schedule template for the group stage from July to November, or for the final stage from November to May. | high | opus |  |
| 0x7c9450 | 176 | `PolFirst::create_table` | thiscall(PolFirst* this) ret 0, returns 1 on success and 0 on failure | Seeds the sixteen Polish First Division clubs into two groups of eight by last position, fills the first group table and pays each club 500000. | high | opus |  |
| 0x7c9690 | 39 | `PolFirst::set_up_rules` | thiscall(PolFirst* this) ret 0, returns 1 | Sets the Polish First Division rule bytes, with two stages, no upper league and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x7c9740 | 138 | `PolFirst::start_new_season` | thiscall(PolFirst* this) ret 0 | Runs promotion and relegation, moves Lower Division clubs up, rebuilds the groups and fixtures, then restarts the Second Division. | high | opus |  |
| 0x7c9900 | 151 (+1 unwind) | `PolFirst::create_second_group_stage` | thiscall(PolFirst* this) ret 0 | Builds the second group of eight Polish clubs as a League_Stage with the stage 0 schedule and stores it as the first stage. | high | opus |  |
| 0x7c9ad0 | 40 | `PolFirst::advance_stage` | thiscall(PolFirst* this) ret 0 | Moves the Polish First Division to its next stage, builds the final stage after the groups, and reports an error past the last stage. | high | opus |  |
| 0x7c9b60 | 392 (+3 unwind) | `PolFirst::create_final_stage` | thiscall(PolFirst* this) ret 0 | Puts the top four of each group in the championship group and the rest in the relegation group, with half their points, in one stage. | high | opus |  |
| 0x7ca030 | 143 | `pol_first_promote_lower_division_clubs` | cdecl, no arguments, ret 0 | Promotes four shuffled Polish Lower Division clubs to the Second Division and moves the bottom clubs of the Second Division down to the Lower Division. | high | opus |  |
| 0x7ca1e0 | 60 | `PolFirst::set_predicted_positions` | thiscall(PolFirst* this) ret 0 | Sorts the sixteen Polish First Division clubs by strength and stores each rank as the club's predicted position in Comp_Stats. | high | opus |  |
| 0x7ca2a0 | 40 | `PolFirst::update_staff_records_for_status` | thiscall(PolFirst* this, Club* club, char status, char stage, ...) ret 0x18 | Adds a qualified record after the group stage, or a champions or relegation record after the final stage, to the club's staff records. | high | opus |  |
| 0x7ca320 | 77 | `PolFirst::build_fate_news_text` | thiscall(PolFirst* this, int club_index, char fate, char stage, ..., int full_sentence, ...) ret 0x28 | Writes the news text for a club that qualifies for the championship group, and uses the base fate news after the final stage. | high | opus |  |
| 0x7ca3f0 | 33 | `PolFirst::set_club_progress` | thiscall(PolFirst* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, remapping them for the group stage. | high | opus |  |
| 0x7ca450 | 21 | `pol_first_compare_championship_group_first` | cdecl(TableRow* a, TableRow* b) ret 0, returns int | Orders two table rows so that clubs of the championship group come before clubs of the relegation group. | high | opus |  |
| 0x7ca490 | 26 | `PolFirst::process_promotion_relegation_chain` | thiscall(PolFirst* this, int pairwise unused) ret 4 | Records final positions in the Polish final stage and the Second Division, then swaps clubs between the two. | high | opus |  |
