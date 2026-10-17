# eng_auto_cup.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x56aa30 | 173 (+2 unwind) | `EngAutoCup::EngAutoCup` | thiscall(EngAutoCup* this, short season_year, int parent) ret 8 | Constructs the English Auto Windscreens cup, loads it from disk or picks two 28-club sections and builds rounds, stages, fixture tree, stats and ranking. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x56aca0 | 11 | `EngAutoCup::`scalar deleting destructor'` | thiscall(EngAutoCup* this, unsigned flags) ret 4 | Runs the EngAutoCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x56acc0 | 90 (+1 unwind) | `EngAutoCup::~EngAutoCup` | thiscall(EngAutoCup* this) ret 0 | Destroys the Auto Windscreens cup by freeing its entrant list, round table, tie arrays, stage objects, stats and club buffer, then runs the Cup destructor. | high | opus |  |
| 0x56ade0 | 332 | `EngAutoCup::create_round_table` | thiscall(EngAutoCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the five-round section table for stage 0 or the one-round final table for stage 1 with draw dates, match dates and round rules. | high | opus |  |
| 0x56b2b0 | 95 | `EngAutoCup::build_fate_news_text` | thiscall(EngAutoCup* this, int club_index, char fate, char stage, int a4, int a5, int a6, int a7, int a8, int cup_result, int a10) ret 0x28 | Writes a section winner's 'through to the final' headline, or passes other fates to the cup tie writer or the Comp version. | high | opus |  |
| 0x56b3c0 | 68 | `EngAutoCup::collect_entrants` | thiscall(EngAutoCup* this) ret 0, returns 1 or -1 | Fills the 28-entry six-byte entrant list of the cup with the second half of the selected club buffer. | medium | opus |  |
| 0x56b4b0 | 183 | `EngAutoCup::start_new_season` | thiscall(EngAutoCup* this) ret 0 | Frees last season's cup data and stages, archives the stats, advances the year and rebuilds clubs, entrants, rounds, stages, fixture tree and ranking. | high | opus |  |
| 0x56b700 | 16 | `EngAutoCup::set_up_rounds` | thiscall(EngAutoCup* this) ret 0, returns 1 | Sets a prize fund of 400000 and builds the round table of the Auto Windscreens cup. | high | opus |  |
| 0x56b730 | 281 | `EngAutoCup::select_section_clubs` | thiscall(EngAutoCup* this) ret 0, returns 1 when 56 clubs fill, else 0 | Picks 56 English clubs from the Second and Third Divisions, the Conference and lower clubs, then sorts them by latitude and reputation into two halves. | high | sonnet |  |
| 0x56bab0 | 134 (+1 unwind) | `EngAutoCup::create_section_stage` | thiscall(EngAutoCup* this) ret 0 | Creates the first section stage as a Cup_Stage from the first 28 selected clubs and stores it as stage 0. | medium | opus |  |
| 0x56bc50 | 40 | `EngAutoCup::advance_stage` | thiscall(EngAutoCup* this) ret 0 | Moves the cup to its next stage and creates the final stage when stage 1 begins, or reports an error past the last stage. | high | opus |  |
| 0x56bce0 | 158 (+1 unwind) | `EngAutoCup::create_final_stage` | thiscall(EngAutoCup* this) ret 0 | Builds the two-club final stage from the winners of the two sections and draws its round. | high | opus |  |
| 0x56bee0 | 109 | `EngAutoCup::update_staff_records_for_status` | thiscall(EngAutoCup* this, Club* club, char outcome, char stage, int arg4, Fixture* fixture, int arg6) ret 0x18 | Adds the staff history record for a club's Auto Windscreens result, such as knocked out, reached a round, winners or runners-up. | high | opus |  |
| 0x56c010 | 182 | `EngAutoCup::rank_teams` | thiscall(EngAutoCup* this) ret 0 | Gives every club of both sections a final position, the top two by reputation first and the rest in alternate places by round. | high | opus |  |
| 0x56c240 | 29 | `EngAutoCup::set_club_progress` | thiscall(EngAutoCup* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, as odd codes 2n-1 when the stage is not positive. | high | opus |  |
