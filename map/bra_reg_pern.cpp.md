# bra_reg_pern.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4388f0 | 160 (+2 unwind) | `BraRegPern::BraRegPern` | thiscall(BraRegPern* this, short season_year, void* comp_record) ret 8, returns this | Builds the Pernambuco regional league on League, loads saved state or sets up rules, the ten-club table, fixtures, Comp_Stats and predicted positions. | high | opus |  |
| 0x438b10 | 11 | `BraRegPern::`scalar deleting destructor'` | thiscall(BraRegPern* this, unsigned flags) ret 4, returns this | Runs the Pernambuco league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x438b30 | 57 (+1 unwind) | `BraRegPern::~BraRegPern` | thiscall(BraRegPern* this) ret 0 | Frees the league table, the schedule template, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x438bf0 | 763 | `BraRegPern::create_schedule` | thiscall(BraRegPern* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the 18-round league template from January for stage -1, or the two-round semi-final and final cup template of April and May for stage 0. | high | opus |  |
| 0x439330 | 84 | `BraRegPern::create_table` | thiscall(BraRegPern* this) ret 0, returns bool | Sets the team count to ten, allocates the table and adds every club whose regional division matches the Pernambuco championship until the table is full. | high | opus |  |
| 0x439430 | 40 | `BraRegPern::set_up_rules` | thiscall(BraRegPern* this) ret 0, returns 1 | Sets the league rule bytes for points, tie-breaks, then builds and stores the league stage schedule. | high | opus |  |
| 0x4394d0 | 141 | `BraRegPern::start_new_season` | thiscall(BraRegPern* this) ret 0 | Clears the old table, schedule and stages, archives stats, moves the season year on and rebuilds rules, table, fixtures and predictions, then renews officials. | high | opus |  |
| 0x439680 | 40 | `BraRegPern::advance_stage` | thiscall(BraRegPern* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the semi-final cup stage when the counter reaches 0. | high | opus |  |
| 0x439710 | 139 (+1 unwind) | `BraRegPern::create_semi_final_stage` | thiscall(BraRegPern* this) ret 0 | Takes the top four clubs of the table and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third, then sets up its first round. | high | opus |  |
| 0x4398d0 | 121 | `BraRegPern::set_predicted_positions` | thiscall(BraRegPern* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions, with third place shared by the two losing semi-finalists. | high | opus |  |
