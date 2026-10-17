# bra_reg_parana.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x437400 | 160 (+2 unwind) | `BraRegParana::BraRegParana` | thiscall(BraRegParana* this, short season_year, void* comp_record) ret 8, returns this | Constructs the Parana regional league on League with three stages, then loads saved state or sets up rules, the 12-club table, fixtures, Comp_Stats and predictions. | high | opus |  |
| 0x437620 | 11 | `BraRegParana::`scalar deleting destructor'` | thiscall(BraRegParana* this, unsigned flags) ret 4, returns this | Runs the Parana regional league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x437640 | 57 (+1 unwind) | `BraRegParana::~BraRegParana` | thiscall(BraRegParana* this) ret 0 | Destroys the Parana regional league by freeing its table, schedule template, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x437700 | 857 | `BraRegParana::create_schedule` | thiscall(BraRegParana* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the 22-round league template from January to May for stage -1, or the one-round final template of May for stage 2. | high | opus |  |
| 0x437ec0 | 84 | `BraRegParana::create_table` | thiscall(BraRegParana* this) ret 0, returns bool | Sets the team count to 12, allocates the table and fills it with the clubs whose regional competition is the Parana championship. | high | opus |  |
| 0x437fc0 | 40 | `BraRegParana::set_up_rules` | thiscall(BraRegParana* this) ret 0, returns 1 | Sets the Parana league rule fields for points and tie-breaks, then builds and stores the league schedule through create_schedule. | high | opus |  |
| 0x438060 | 149 | `BraRegParana::start_new_season` | thiscall(BraRegParana* this) ret 0 | Clears the old table, schedule and stages, resets three stage slots, advances the season year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x438230 | 40 | `BraRegParana::advance_stage` | thiscall(BraRegParana* this) ret 0 | Moves the Parana championship to its next stage and sets up the final when stage 2 starts, or reports an error after the last stage. | high | opus |  |
| 0x4382c0 | 168 (+1 unwind) | `BraRegParana::create_final_stage` | thiscall(BraRegParana* this) ret 0 | Crowns the club that won both half-season stages, or else creates the two-club final Cup_Stage as stage 2 between the two stage winners. | medium | opus |  |
| 0x4384e0 | 54 | `BraRegParana::record_season_honours` | thiscall(BraRegParana* this) ret 0 | Records the honours through the final stage when stage 2 was played, or else pays 175,000 and 100,000 prize money to the top two clubs. | high | opus |  |
| 0x438590 | 111 | `BraRegParana::set_predicted_positions` | thiscall(BraRegParana* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions as winner, runner-up, then third place onwards. | high | opus |  |
| 0x4386e0 | 49 | `BraRegParana::add_result` | thiscall(BraRegParana* this, Fixture* fixture, int update_stats) ret 8, returns 1 | Adds a result to the full table, then forwards it to the half-season League_Stage of its round, creating that stage when it does not exist. | high | opus |  |
| 0x438760 | 125 (+1 unwind) | `BraRegParana::create_half_stage` | thiscall(BraRegParana* this, char half) ret 4 | Creates the League_Stage for one half of the Parana season from all table clubs and stores it as the current stage. | medium | opus |  |
