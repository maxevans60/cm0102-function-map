# bra_reg_northeast.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4363f0 | 160 (+2 unwind) | `BraRegNortheast::BraRegNortheast` | thiscall(BraRegNortheast* this, short season_year, void* comp_record) ret 8, returns this | Constructs the Northeast regional league on League, then loads saved state or sets up rules, the 16-club table, fixtures, Comp_Stats and predictions. | high | opus |  |
| 0x436610 | 11 | `BraRegNortheast::`scalar deleting destructor'` | thiscall(BraRegNortheast* this, unsigned flags) ret 4, returns this | Runs the Northeast regional league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x436630 | 57 (+1 unwind) | `BraRegNortheast::~BraRegNortheast` | thiscall(BraRegNortheast* this) ret 0 | Destroys the Northeast regional league by freeing its table, schedule template, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x4366f0 | 687 | `BraRegNortheast::create_schedule` | thiscall(BraRegNortheast* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the 15-round league template of January to April for stage -1, or the semi-final and final template of April and May for stage 0. | high | opus |  |
| 0x436d90 | 84 | `BraRegNortheast::create_table` | thiscall(BraRegNortheast* this) ret 0, returns bool | Sets the team count to 16, allocates the table and fills it with the clubs whose regional competition is the Northeast championship. | high | opus |  |
| 0x436e90 | 141 | `BraRegNortheast::start_new_season` | thiscall(BraRegNortheast* this) ret 0 | Clears the old table, schedule and stages, archives the stats, advances the season year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x437040 | 40 | `BraRegNortheast::advance_stage` | thiscall(BraRegNortheast* this) ret 0 | Moves the Northeast championship to its next stage and creates the semi-final stage when stage 0 starts, or reports an error after the last stage. | high | opus |  |
| 0x4370d0 | 139 (+1 unwind) | `BraRegNortheast::create_semi_final_stage` | thiscall(BraRegNortheast* this) ret 0 | Takes the top four table clubs and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third. | high | opus |  |
| 0x437290 | 121 | `BraRegNortheast::set_predicted_positions` | thiscall(BraRegNortheast* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions, with third place shared by the two losing semi-finalists. | high | opus |  |
