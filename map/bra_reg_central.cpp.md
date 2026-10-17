# bra_reg_central.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4304b0 | 160 (+2 unwind) | `BraRegCentral::BraRegCentral` | thiscall(BraRegCentral* this, short season_year, void* comp_record) ret 8, returns this | Builds the Central regional league on League, loads saved state or sets up rules, the 15-club table, fixtures, Comp_Stats and predicted positions. | high | opus |  |
| 0x4306d0 | 11 | `BraRegCentral::`scalar deleting destructor'` | thiscall(BraRegCentral* this, unsigned flags) ret 4, returns this | Runs the Central regional league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x4306f0 | 57 (+1 unwind) | `BraRegCentral::~BraRegCentral` | thiscall(BraRegCentral* this) ret 0 | Frees the league table, the schedule template, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x4307b0 | 725 | `BraRegCentral::create_schedule` | thiscall(BraRegCentral* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the round template for a stage, 15 league rounds for the first stage or three knockout rounds for the eight-club stage 0. | high | opus |  |
| 0x430ef0 | 84 | `BraRegCentral::load_region_clubs` | thiscall(BraRegCentral* this) ret 0, returns bool | Sets the team count to 15, allocates the table and adds every club whose division pointer matches the Central region until the table is full. | high | opus |  |
| 0x430ff0 | 40 | `BraRegCentral::set_up_rules` | thiscall(BraRegCentral* this) ret 0, returns 1 | Sets the league rule bytes for points, tie-breaks and the eight-club knockout, then builds and stores the first stage schedule. | high | opus |  |
| 0x431090 | 141 | `BraRegCentral::start_new_season` | thiscall(BraRegCentral* this) ret 0 | Clears last season's table, schedule and stages, archives stats, moves the season year on and rebuilds rules, clubs, fixtures and predictions. | high | opus |  |
| 0x431240 | 40 | `BraRegCentral::advance_stage` | thiscall(BraRegCentral* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the knockout stage when the counter reaches 0. | high | opus |  |
| 0x4312d0 | 154 (+1 unwind) | `BraRegCentral::create_knockout_stage` | thiscall(BraRegCentral* this) ret 0 | Takes the top eight clubs of the league table and creates the eight-club knockout Cup_Stage, then sets up its first round. | high | opus |  |
| 0x4314e0 | 114 | `BraRegCentral::update_staff_records_for_status` | thiscall(BraRegCentral* this, Club* club, char status, char stage, int unused, Fixture* fixture) ret 0x18 | Adds staff history records for a club's result, qualification or relegation in the league stage, or title or exit in the knockout stage. | high | opus |  |
| 0x431610 | 148 | `BraRegCentral::set_predicted_positions` | thiscall(BraRegCentral* this) ret 0 | Sorts the table clubs by strength and gives predicted places 1, 2, two 3rds, four 5ths and then 9 onwards in Comp_Stats. | high | opus |  |
