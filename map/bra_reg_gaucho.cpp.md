# bra_reg_gaucho.cpp: 14 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4317c0 | 160 (+2 unwind) | `BraRegGaucho::BraRegGaucho` | thiscall(BraRegGaucho* this, short season_year, void* comp_record) ret 8, returns this | Builds the Gaucho regional league on League, loads saved state or sets up rules, the 17-club table, fixtures, Comp_Stats and predicted positions. | high | opus |  |
| 0x4319e0 | 11 | `BraRegGaucho::`scalar deleting destructor'` | thiscall(BraRegGaucho* this, unsigned flags) ret 4, returns this | Runs the Gaucho regional league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x431a00 | 57 (+1 unwind) | `BraRegGaucho::~BraRegGaucho` | thiscall(BraRegGaucho* this) ret 0 | Frees the league table, the schedule template, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x431ac0 | 744 | `BraRegGaucho::create_schedule` | thiscall(BraRegGaucho* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the round template for a stage, 17 league rounds for the first stage or the two-round semi-final and final for the four-club stage 0. | high | opus |  |
| 0x432070 | 21 | `BraRegGaucho::create_schedule_fragment_432070` | misread entry inside create_schedule, shares its frame, ret 0x10 | Misread entry point inside the error path of create_schedule that formats the line 0x122 assert and shows the Error message box. | high | opus |  |
| 0x4321d0 | 84 | `BraRegGaucho::load_region_clubs` | thiscall(BraRegGaucho* this) ret 0, returns bool | Sets the team count to 17, allocates the table and adds every club whose division pointer matches the Gaucho region until the table is full. | high | opus |  |
| 0x4322d0 | 43 | `BraRegGaucho::set_up_rules` | thiscall(BraRegGaucho* this) ret 0, returns 1 | Sets the league rule bytes for points, tie-breaks and the four-club knockout, then builds and stores the first stage schedule. | high | opus |  |
| 0x432370 | 141 | `BraRegGaucho::start_new_season` | thiscall(BraRegGaucho* this) ret 0 | Clears last season's table, schedule and stages, archives stats, moves the season year on and rebuilds rules, clubs, fixtures and predictions. | high | opus |  |
| 0x432520 | 40 | `BraRegGaucho::advance_stage` | thiscall(BraRegGaucho* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the knockout stage when the counter reaches 0. | high | opus |  |
| 0x4325b0 | 139 (+1 unwind) | `BraRegGaucho::create_knockout_stage` | thiscall(BraRegGaucho* this) ret 0 | Takes the top four clubs of the league table and creates the four-club semi-final Cup_Stage, then sets up its first round. | high | opus |  |
| 0x432770 | 182 | `BraRegGaucho::build_fate_news_text` | thiscall(BraRegGaucho* this, int club_index, char status, char stage, int a5, int a6, int a7, int a8, int a9, int has_comp, int a11) ret 0x28 | Writes the semi-final qualification or championship win news text for a club and passes other outcomes to the base Comp text builder. | high | opus |  |
| 0x432970 | 5 | `BraRegGaucho::record_season_honours` | thiscall(BraRegGaucho* this) ret 0, tail call | Records the honours of the first stage through its own virtual method, then runs the Brazilian regional winners helper. | high | opus |  |
| 0x432980 | 121 | `BraRegGaucho::set_predicted_positions` | thiscall(BraRegGaucho* this) ret 0 | Sorts the table clubs by strength and gives predicted places 1, 2, two 3rds and then 5 onwards in Comp_Stats. | high | opus |  |
| 0x432af0 | 30 | `BraRegGaucho::set_club_progress` | thiscall(BraRegGaucho* this, Club* club, char stage, char code1, unsigned char code2, unsigned char code3) ret 0x14 | Stores the three stage codes of a club in its Comp_Stats entry, raising low codes to 1 and 3 for the league stage. | high | opus |  |
