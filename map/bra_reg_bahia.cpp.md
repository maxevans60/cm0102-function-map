# bra_reg_bahia.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x42f2d0 | 160 (+2 unwind) | `BraRegBahia::BraRegBahia` | thiscall(BraRegBahia* this, short year, Comp* comp_record) ret 8 | Constructs the Bahia state championship on League, then loads saved data or sets up rules, the ten-club table, fixtures and stats. | high | opus |  |
| 0x42f4f0 | 11 | `BraRegBahia::`scalar deleting destructor'` | thiscall(BraRegBahia* this, unsigned flags) ret 4 | Destroys the Bahia state championship object and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x42f510 | 57 (+1 unwind) | `BraRegBahia::~BraRegBahia` | thiscall(BraRegBahia* this) ret 0 | Destroys the Bahia state championship, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x42f5d0 | 763 | `BraRegBahia::create_schedule` | thiscall(BraRegBahia* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10 | Builds the 18-round league schedule from January for stage -1, or the two-round semi-final and final cup schedule of April and May for stage 0. | high | opus |  |
| 0x42fd10 | 84 | `BraRegBahia::create_table` | thiscall(BraRegBahia* this) ret 0, returns bool | Fills the ten-row table with the clubs whose regional competition is the Bahia championship and returns true when all ten are found. | high | opus |  |
| 0x42fe10 | 141 | `BraRegBahia::start_new_season` | thiscall(BraRegBahia* this) ret 0 | Clears the old season and stages, then rebuilds rules, table and fixtures for the new year and renews the officials. | high | opus |  |
| 0x42ffc0 | 40 | `BraRegBahia::advance_stage` | thiscall(BraRegBahia* this) ret 0 | Moves the competition to its next stage and creates the semi-final cup when the league stage ends. | high | opus |  |
| 0x430050 | 139 (+1 unwind) | `BraRegBahia::create_semi_final_stage` | thiscall(BraRegBahia* this) ret 0 | Takes the top four clubs of the table and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third. | high | opus |  |
| 0x430210 | 114 | `BraRegBahia::update_staff_records_for_status` | thiscall(BraRegBahia* this, Club* club, char status, char stage, int arg, Fixture* fixture) ret 0x18 | Adds staff records for semi-final qualification, relegation, the title or a knockout exit and marks the club's table row status. | high | opus |  |
| 0x430340 | 121 | `BraRegBahia::set_predicted_positions` | thiscall(BraRegBahia* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions, with third place shared by the two losing semi-finalists. | high | opus |  |
