# usa_mls.cpp: 22 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x906f80 | 160 (+2 unwind) | `UsaMls::UsaMls` | thiscall(UsaMls* this, short year, Comp* comp) ret 8, returns this | Builds the MLS league on League, sets its rules, fills the first division table, makes the season fixtures and creates the Comp_Stats object. | high | opus |  |
| 0x9071f0 | 11 | `UsaMls::`scalar deleting destructor'` | thiscall(UsaMls* this, unsigned flags) ret 4, returns this | Runs the MLS destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x907210 | 60 (+1 unwind) | `UsaMls::~UsaMls` | thiscall(UsaMls* this) ret 0 | Restores the MLS vtable, frees the table, schedule and stage objects and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x9072d0 | 1645 | `UsaMls::create_schedule` | thiscall(UsaMls* this, char stage, short* round_count, short* comp_code, int* is_league) ret 0x10, returns schedule buffer | Builds the date template of one stage: 12, 22 or 32 league rounds, the two-round play-off stage or the one-round MLS Cup final. | high | opus |  |
| 0x908200 | 126 | `UsaMls::update_staff_records_for_status` | thiscall(UsaMls* this, Club* club, char status, char stage, int a4, Fixture* fixture) ret 0x18, returns 0 or -1 | Writes the staff history record for a club: play-off qualification, failure to qualify by division, final reached, knock-out or champions. | high | opus |  |
| 0x908360 | 183 | `UsaMls::build_fate_news_text` | thiscall(UsaMls* this, int club_index, int fate, char stage, int a4, int a5, int a6, int a7, int a8, int full_sentence, int a10) ret 0x28 | Writes the news text for a club's MLS fate, from reaching the quarter finals or the final to winning the competition. | high | opus |  |
| 0x908560 | 84 | `UsaMls::create_table` | thiscall(UsaMls* this) ret 0, returns 1 when four clubs are found, 0 otherwise | Sets the team count to four, allocates the table and fills it with the MLS clubs of division code 0x413. | high | opus |  |
| 0x908660 | 23 | `UsaMls::set_up_rules` | thiscall(UsaMls* this) ret 0 | Sets the MLS rule fields such as substitute counts, tiebreak bytes and the four-club team count. | high | opus |  |
| 0x9086e0 | 507 (+1 unwind) | `UsaMls::create_season_fixtures` | thiscall(UsaMls* this) ret 0, returns 1 | Makes the first division fixtures, builds the other two division stages and adds the cross-division matches from the regular season template. | medium | opus |  |
| 0x908e00 | 143 | `UsaMls::start_new_season` | thiscall(UsaMls* this) ret 0 | Frees last season's MLS data and stages, archives the stats, moves the year on and rebuilds the rules, table and fixtures. | high | opus |  |
| 0x908fc0 | 169 (+1 unwind) | `UsaMls::create_second_division_stage` | thiscall(UsaMls* this) ret 0 | Collects the four MLS clubs of division code 0x47b and builds their League_Stage as stage 0. | high | opus |  |
| 0x9091e0 | 169 (+1 unwind) | `UsaMls::create_third_division_stage` | thiscall(UsaMls* this) ret 0 | Collects the four MLS clubs of division code 0x414 and builds their League_Stage as stage 1. | high | opus |  |
| 0x909400 | 51 | `UsaMls::advance_stage` | thiscall(UsaMls* this) ret 0 | Moves the MLS to its next stage and builds the play-off stage or the MLS Cup final stage. | high | opus |  |
| 0x9094c0 | 228 (+1 unwind) | `UsaMls::create_playoff_stage` | thiscall(UsaMls* this) ret 0 | Seeds the three division winners and the five best other clubs into an eight-club play-off Cup_Stage and sets up its first round. | high | opus |  |
| 0x9097d0 | 161 (+1 unwind) | `UsaMls::create_final_stage` | thiscall(UsaMls* this) ret 0 | Takes the two clubs still in the play-off and builds the two-club MLS Cup final Cup_Stage as stage 3. | high | opus |  |
| 0x9099d0 | 42 | `UsaMls::add_result` | thiscall(UsaMls* this, Fixture* match, int update_stats) ret 8, returns 1 | Adds a result to the MLS table and, in the regular season, also to both division stages with the stats object held back. | high | opus |  |
| 0x909a40 | 110 | `UsaMls::get_club_array` | thiscall(UsaMls* this, Club*** out_clubs, short* out_count) ret 8 | Allocates an array of the twelve MLS clubs from the first division table and the tables of both division stages. | high | opus |  |
| 0x909bb0 | 183 | `UsaMls::set_predicted_positions` | thiscall(UsaMls* this) ret 0 | Ranks the clubs of each division table by reputation and stores overall predicted places 1, 4, 7 and 10 for each division's top four. | high | opus |  |
| 0x909dd0 | 81 | `UsaMls::set_club_progress` | thiscall(UsaMls* this unused, Club* club, char stage, char result, char position, char finish) ret 0x14 | Writes a club's stage result, position and finish code into its Comp_Stats entry, mapping play-off round codes onto knockout codes. | high | opus |  |
| 0x909ec0 | 72 | `usa_mls_get_club_division` | cdecl(Club* club) ret 0, returns short division code | Returns the MLS division code 0x413, 0x47b or 0x414 of one of the twelve MLS clubs, or reports an error for others. | high | opus |  |
| 0x90a000 | 69 | `usa_mls_get_club_all_star_conference` | cdecl(Club* club) ret 0, returns short conference code | Returns the All-Star conference code 0x413 or 0x414 of one of the twelve MLS clubs, or reports an error for others. | high | opus |  |
| 0x90a130 | 6 | `usa_mls_compare_points_desc` | cdecl(Entry* a, Entry* b) ret 0, returns int | Orders two six-byte club entries for qsort by the short at offset 4, highest first. | medium | opus |  |
