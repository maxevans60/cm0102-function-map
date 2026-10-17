# gre_prm.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5ea410 | 156 (+2 unwind) | `GrePrm::GrePrm` | thiscall(GrePrm* this, short year, void* comp_record) ret 8, returns this | Constructs the Greek First Division on League, loads it from the temp file or sets rules, fills the table, makes fixtures and creates Comp_Stats. | high | opus |  |
| 0x5ea620 | 11 | `GrePrm::`scalar deleting destructor'` | thiscall(GrePrm* this, unsigned flags) ret 4, returns this | Runs the GrePrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5ea640 | 38 (+1 unwind) | `GrePrm::~GrePrm` | thiscall(GrePrm* this) ret 0 | Destroys the Greek First Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5ea6d0 | 672 | `GrePrm::create_schedule` | thiscall(GrePrm* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 26-round season schedule of the Greek First Division from September to May, or a three-round stage 0 schedule in May. | high | opus |  |
| 0x5ead60 | 99 | `GrePrm::create_table` | thiscall(GrePrm* this) ret 0, returns 1 on success and 0 on failure | Allocates the 14-row table, fills it with the clubs of the Greek First Division, sets the prize fund and pays each club 500000. | high | opus |  |
| 0x5eae90 | 43 | `GrePrm::set_up_rules` | thiscall(GrePrm* this) ret 0, returns 1 | Sets the Greek First Division rule bytes with no division above and the Second Division below, then builds the schedule through create_schedule. | high | opus |  |
| 0x5eaf50 | 145 | `GrePrm::start_new_season` | thiscall(GrePrm* this) ret 0 | Swaps Second and Third Division clubs, frees the old table and schedule, archives Comp_Stats, increments the year and rebuilds the season. | high | opus |  |
| 0x5eb120 | 133 | `gre_prm_swap_second_and_third_division_clubs` | cdecl, no arguments, ret 0 | Promotes the two best Third Division clubs to the Second Division and moves the relegated Second Division clubs down to the Third Division. | high | opus |  |
