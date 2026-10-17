# bra_reg_santa.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x43b130 | 160 (+2 unwind) | `BraRegSanta::BraRegSanta` | thiscall(BraRegSanta* this, short year, Comp* comp_record) ret 8, returns this | Constructs the Santa Catarina state championship on League, then loads saved data or sets up rules, the ten-club table, fixtures and stats. | high | opus |  |
| 0x43b350 | 11 | `BraRegSanta::`scalar deleting destructor'` | thiscall(BraRegSanta* this, unsigned flags) ret 4, returns this | Runs the Santa Catarina championship destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x43b370 | 57 (+1 unwind) | `BraRegSanta::~BraRegSanta` | thiscall(BraRegSanta* this) ret 0 | Frees the table, the schedule template, every stage object and the Comp_Stats of the Santa Catarina championship, then runs the League destructor. | high | opus |  |
| 0x43b430 | 763 | `BraRegSanta::create_schedule` | thiscall(BraRegSanta* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10, returns schedule template | Builds the 18-round league template for stage -1, or the two-round semi-final and final cup template for stage 0. | high | opus |  |
| 0x43bb70 | 84 | `BraRegSanta::create_table` | thiscall(BraRegSanta* this) ret 0, returns bool | Sets the team count to ten, allocates the table and fills it with the clubs whose regional competition is the Santa Catarina championship. | high | opus |  |
| 0x43bc70 | 43 | `BraRegSanta::set_up_rules` | thiscall(BraRegSanta* this) ret 0, returns 1 | Sets the league rule bytes for points, tie-breaks and the four-club semi-final, then builds and stores the first stage schedule. | high | opus |  |
| 0x43bd10 | 141 | `BraRegSanta::start_new_season` | thiscall(BraRegSanta* this) ret 0 | Clears last season's table, schedule and stages, archives stats, moves the year on and rebuilds rules, clubs, fixtures and predictions. | high | opus |  |
| 0x43bec0 | 40 | `BraRegSanta::advance_stage` | thiscall(BraRegSanta* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the semi-final stage when the counter reaches 0. | high | opus |  |
| 0x43bf50 | 139 (+1 unwind) | `BraRegSanta::create_semi_final_stage` | thiscall(BraRegSanta* this) ret 0 | Takes the top four clubs of the table and creates the semi-final Cup_Stage as stage 0, pairing first with fourth and second with third. | high | opus |  |
| 0x43c110 | 121 | `BraRegSanta::set_predicted_positions` | thiscall(BraRegSanta* this) ret 0 | Sorts the table clubs by strength and gives predicted places 1, 2, two 3rds and then 5 onwards in Comp_Stats. | high | opus |  |
