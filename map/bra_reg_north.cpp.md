# bra_reg_north.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x435340 | 160 (+2 unwind) | `BraRegNorth::BraRegNorth` | thiscall(BraRegNorth* this, short season_year, void* comp_record) ret 8, returns this | Constructs the North regional league on League, then loads saved state or sets up rules, the ten-club table, fixtures, Comp_Stats and predictions. | high | opus |  |
| 0x435560 | 11 | `BraRegNorth::`scalar deleting destructor'` | thiscall(BraRegNorth* this, unsigned flags) ret 4, returns this | Runs the North regional league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x435580 | 57 (+1 unwind) | `BraRegNorth::~BraRegNorth` | thiscall(BraRegNorth* this) ret 0 | Destroys the North regional league by freeing its table, schedule template, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x435640 | 763 | `BraRegNorth::create_schedule` | thiscall(BraRegNorth* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the 18-round league template of January to April for stage -1, or the semi-final and final template of April and May for stage 0. | high | opus |  |
| 0x435d80 | 84 | `BraRegNorth::create_table` | thiscall(BraRegNorth* this) ret 0, returns bool | Sets the team count to 10, allocates the table and fills it with the clubs whose regional competition is the North championship. | high | opus |  |
| 0x435e80 | 141 | `BraRegNorth::start_new_season` | thiscall(BraRegNorth* this) ret 0 | Clears the old table, schedule and stages, archives the stats, advances the season year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x436030 | 40 | `BraRegNorth::advance_stage` | thiscall(BraRegNorth* this) ret 0 | Moves the North championship to its next stage and creates the semi-final stage when stage 0 starts, or reports an error after the last stage. | high | opus |  |
| 0x4360c0 | 139 (+1 unwind) | `BraRegNorth::create_semi_final_stage` | thiscall(BraRegNorth* this) ret 0 | Takes the top four table clubs and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third. | high | opus |  |
| 0x436280 | 121 | `BraRegNorth::set_predicted_positions` | thiscall(BraRegNorth* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions, with third place shared by the two losing semi-finalists. | high | opus |  |
