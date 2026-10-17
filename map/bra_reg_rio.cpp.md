# bra_reg_rio.cpp: 14 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x439a40 | 160 (+2 unwind) | `BraRegRio::BraRegRio` | thiscall(BraRegRio* this, short season_year, void* comp_record) ret 8, returns this | Builds the Rio de Janeiro regional league on League with three stages, loads saved state or sets up rules, the 12-club table, fixtures, Comp_Stats and predictions. | high | opus |  |
| 0x439c60 | 11 | `BraRegRio::`scalar deleting destructor'` | thiscall(BraRegRio* this, unsigned flags) ret 4, returns this | Runs the Rio league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x439c80 | 57 (+1 unwind) | `BraRegRio::~BraRegRio` | thiscall(BraRegRio* this) ret 0 | Frees the league table, the schedule template, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x439d40 | 857 | `BraRegRio::create_schedule` | thiscall(BraRegRio* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule template | Builds the 22-round league template from January to May for stage -1, or the one-round template of the two-club final in May for stage 2. | high | opus |  |
| 0x43a500 | 84 | `BraRegRio::create_table` | thiscall(BraRegRio* this) ret 0, returns bool | Sets the team count to 12, allocates the table and adds every club whose regional division matches the Rio championship until the table is full. | high | opus |  |
| 0x43a600 | 40 | `BraRegRio::set_up_rules` | thiscall(BraRegRio* this) ret 0, returns 1 | Sets the league rule bytes for points and tie-breaks, then builds and stores the league stage schedule. | high | opus |  |
| 0x43a6a0 | 149 | `BraRegRio::start_new_season` | thiscall(BraRegRio* this) ret 0 | Clears the old table, schedule and three stage slots, archives stats, moves the year on and rebuilds rules, table, fixtures and predictions, then renews officials. | high | opus |  |
| 0x43a870 | 40 | `BraRegRio::advance_stage` | thiscall(BraRegRio* this) ret 0 | Moves the Rio championship to its next stage and creates the final when stage 2 starts, or reports an error after the last stage. | high | opus |  |
| 0x43a900 | 168 (+1 unwind) | `BraRegRio::create_final_stage` | thiscall(BraRegRio* this) ret 0 | Creates the two-club final between the winners of the two half-season stages, or ends the season with two stages when one club won both. | high | opus |  |
| 0x43ab20 | 182 | `BraRegRio::build_fate_news_text` | thiscall(BraRegRio* this, int club_index, char status, char stage, int a5, int a6, int a7, int a8, int a9, int full_sentence, int a11) ret 0x28 | Writes the semi-final qualification or championship win news text for a club and passes other outcomes to the base fate text builder. | high | opus |  |
| 0x43ad20 | 54 | `BraRegRio::record_season_honours` | thiscall(BraRegRio* this) ret 0 | Records honours through the final stage when one is played, otherwise stores league honours and pays 675000 and 250000 to the top two clubs. | high | opus |  |
| 0x43add0 | 111 | `BraRegRio::set_predicted_positions` | thiscall(BraRegRio* this) ret 0 | Sorts the table clubs by strength and stores predicted final positions 1 to 12 in Comp_Stats. | high | opus |  |
| 0x43af20 | 49 | `BraRegRio::add_result` | thiscall(BraRegRio* this, Fixture* match, int update_stats) ret 8, returns 1 | Adds a match to the full league table, then creates the matching half-season stage if needed and adds the match to that stage too. | high | opus |  |
| 0x43afa0 | 125 (+1 unwind) | `BraRegRio::create_half_season_stage` | thiscall(BraRegRio* this, char stage_index) ret 4 | Creates a League_Stage that holds all twelve Rio clubs for one half of the season and stores it in the given stage slot. | high | opus |  |
