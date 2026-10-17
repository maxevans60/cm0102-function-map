# bra_reg_goias.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x432b50 | 160 (+2 unwind) | `BraRegGoias::BraRegGoias` | thiscall(BraRegGoias* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the Goias regional league on League, loads saved state or sets rules, fills the 14-club table, builds fixtures and creates its Comp_Stats. | high | opus |  |
| 0x432d70 | 11 | `BraRegGoias::`scalar deleting destructor'` | thiscall(BraRegGoias* this, unsigned flags) ret 4, returns this | Runs the Goias league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x432d90 | 57 (+1 unwind) | `BraRegGoias::~BraRegGoias` | thiscall(BraRegGoias* this) ret 0 | Destroys the Goias league: frees its table and schedule, deletes each stage object and the Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x432e50 | 686 | `BraRegGoias::create_schedule` | thiscall(BraRegGoias* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule template | Builds the round template of the Goias league stage (13 rounds) or of its eight-club knockout stage with quarter-finals, semi-finals and final. | high | opus |  |
| 0x433540 | 84 | `BraRegGoias::create_table` | thiscall(BraRegGoias* this) ret 0, returns bool | Sets the team count to 14, allocates the table and fills it with the clubs whose reserve division is the Goias championship. | high | opus |  |
| 0x433640 | 40 | `BraRegGoias::set_up_rules` | thiscall(BraRegGoias* this) ret 0, returns 1 | Sets the Goias league rule fields, such as points, tiebreaks and the eight qualifying places, then builds the league schedule through create_schedule. | high | opus |  |
| 0x4336f0 | 141 | `BraRegGoias::start_new_season` | thiscall(BraRegGoias* this) ret 0 | Archives the season, frees the table and stages, advances the year, then rebuilds rules, table, fixtures and predictions for the new Goias season. | high | opus |  |
| 0x4338a0 | 40 | `BraRegGoias::advance_stage` | thiscall(BraRegGoias* this) ret 0 | Moves the Goias championship to its next stage and creates the knockout stage when stage 0 starts, or reports an error after the last stage. | high | opus |  |
| 0x433930 | 154 (+1 unwind) | `BraRegGoias::create_knockout_stage` | thiscall(BraRegGoias* this) ret 0 | Creates the Goias eight-club knockout Cup_Stage from the top eight table rows in seeded pairs and sets up its first round. | high | opus |  |
| 0x433b40 | 148 | `BraRegGoias::set_predicted_positions` | thiscall(BraRegGoias* this) ret 0 | Sorts the Goias clubs by strength and stores predicted finishes as winner, runner-up, two semi-finalists, four quarter-finalists, then ninth and below. | high | opus |  |
| 0x433cf0 | 30 | `BraRegGoias::set_club_progress` | thiscall(BraRegGoias* this, Club* club, char stage, char code1, byte code2, byte code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, mapping league-stage codes below 9 to the Goias knockout progress values. | high | opus |  |
