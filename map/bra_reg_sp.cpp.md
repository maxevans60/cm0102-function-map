# bra_reg_sp.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x43c280 | 160 (+2 unwind) | `BraRegSp::BraRegSp` | thiscall(BraRegSp* this, short year, Comp* comp_record) ret 8, returns this | Constructs the Sao Paulo state championship on League, then loads saved data or sets up rules, the 16-club table, fixtures and stats. | high | opus |  |
| 0x43c4a0 | 6 | `BraRegSp::points_for_result` | thiscall(BraRegSp* this, Club* club, Fixture* fixture) ret 8, returns points | Passes the points query for a club and fixture straight to the League base method. | high | opus |  |
| 0x43c4c0 | 11 | `BraRegSp::`scalar deleting destructor'` | thiscall(BraRegSp* this, unsigned flags) ret 4, returns this | Runs the Sao Paulo championship destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x43c4e0 | 57 (+1 unwind) | `BraRegSp::~BraRegSp` | thiscall(BraRegSp* this) ret 0 | Frees the table, the schedule template, every stage object and the Comp_Stats of the Sao Paulo championship, then runs the League destructor. | high | opus |  |
| 0x43c5a0 | 687 | `BraRegSp::create_schedule` | thiscall(BraRegSp* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10, returns schedule template | Builds the 15-round league template for stage -1, or the two-round semi-final and final cup template for stage 0. | high | opus |  |
| 0x43cc40 | 84 | `BraRegSp::create_table` | thiscall(BraRegSp* this) ret 0, returns bool | Sets the team count to 16, allocates the table and fills it with the clubs whose regional competition is the Sao Paulo championship. | high | opus |  |
| 0x43cd40 | 141 | `BraRegSp::start_new_season` | thiscall(BraRegSp* this) ret 0 | Clears last season's table, schedule and stages, archives stats, moves the year on and rebuilds rules, clubs, fixtures and predictions. | high | opus |  |
| 0x43cef0 | 40 | `BraRegSp::advance_stage` | thiscall(BraRegSp* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the semi-final stage when the counter reaches 0. | high | opus |  |
| 0x43cf80 | 139 (+1 unwind) | `BraRegSp::create_semi_final_stage` | thiscall(BraRegSp* this) ret 0 | Takes the top four clubs of the table and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third. | high | opus |  |
| 0x43d140 | 121 | `BraRegSp::set_predicted_positions` | thiscall(BraRegSp* this) ret 0 | Sorts the table clubs by strength and gives predicted places 1, 2, two 3rds and then 5 onwards in Comp_Stats. | high | opus |  |
