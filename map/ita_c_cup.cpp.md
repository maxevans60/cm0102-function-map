# ita_c_cup.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63cc40 | 175 (+2 unwind) | `ItaCCup::ItaCCup` | thiscall(ItaCCup* this, short year, void* comp_record) ret 8 | Constructs the Serie C Italian Cup on League and, when no saved data loads, picks 90 clubs and builds rules, fixtures and 15 groups. | high | opus |  |
| 0x63ce90 | 11 | `ItaCCup::`scalar deleting destructor'` | thiscall(ItaCCup* this, unsigned flags) ret 4, returns this | Runs the Serie C Italian Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x63ceb0 | 66 (+1 unwind) | `ItaCCup::~ItaCCup` | thiscall(ItaCCup* this) ret 0 | Destroys the Serie C Italian Cup by freeing its table, schedule, entrant list, child stages and stats, then runs the League destructor. | high | opus |  |
| 0x63cf90 | 391 | `ItaCCup::create_schedule` | thiscall(ItaCCup* this, char stage, short* entry_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer or null | Builds the five-matchday schedule of a group stage below stage 15, or the five two-legged knockout rounds of stage 15 for 32 clubs. | high | opus |  |
| 0x63d4c0 | 98 | `ItaCCup::build_fate_news_text` | thiscall(ItaCCup* this, int club, char status, char stage, int a4, int a5, int a6, int a7, int a8, int has_detail, int a10) ret 0x28 | Writes the news text for a club's fate in a group stage or in the knockout stage of the Serie C Italian Cup. | high | opus |  |
| 0x63d5e0 | 71 | `ItaCCup::init_first_group` | thiscall(ItaCCup* this) ret 0, returns 1 or 0 | Sets the cup's own table to five clubs taken from the entrant list, allocates its rows and sends the group draw news. | medium | opus |  |
| 0x63d6e0 | 37 | `ItaCCup::set_up_rules` | thiscall(ItaCCup* this) ret 0, returns 1 | Sets the group points and tiebreak rules and a prize of 300000, then builds the group schedule through slot 15. | high | opus |  |
| 0x63d770 | 4 | `ItaCCup::record_season_honours` | thiscall(ItaCCup* this) ret 0, tail jump | Passes the season honours to the knockout stage, the sixteenth child stage, so that it records the winner and runner-up. | high | opus |  |
| 0x63d780 | 151 | `ItaCCup::start_new_season` | thiscall(ItaCCup* this) ret 0 | Clears the finished Serie C Italian Cup, archives its stats, moves the year on and picks the clubs, fixtures and groups again. | high | opus |  |
| 0x63d950 | 40 | `ItaCCup::advance_stage` | thiscall(ItaCCup* this) ret 0 | Moves the current stage index on by one and creates the knockout stage when the index reaches 15, or reports an error when it overruns. | high | opus |  |
| 0x63d9e0 | 173 (+1 unwind) | `ItaCCup::create_group_stage` | thiscall(ItaCCup* this, int group_index) ret 4, returns 1 or 0 | Takes the next clubs from the entrant list and builds a League_Stage for one group with its schedule, storing it as the current stage. | high | opus |  |
| 0x63dc10 | 300 (+2 unwind) | `ItaCCup::create_knockout_stage` | thiscall(ItaCCup* this) ret 0 | Ranks the 16 group runners-up, takes the 16 winners, the best six runners-up and ten seeded clubs, then builds and draws the 32-club knockout Cup_Stage. | high | opus |  |
| 0x63dfe0 | 198 | `ItaCCup::select_entrants` | thiscall(ItaCCup* this) ret 0, returns 1 or 0 | Lists the 90 Italian clubs of the five Serie C divisions, moves relegated and play-off clubs to ten seeded places and shuffles pots. | high | opus |  |
| 0x63e270 | 122 | `ItaCCup::update_staff_records_for_status` | thiscall(ItaCCup* this, Club* club, char status, char stage, int a4, Fixture* match, int a6) ret 0x18 | Adds the staff history record for a club that leaves a group, goes out, reaches a round, wins or finishes runner-up. | high | opus |  |
| 0x63e3c0 | 141 | `ItaCCup::load_extra_data` | thiscall(ItaCCup* this, FILE* file) ret 4, returns 1 or 0 | Reads the entrant count and club indexes from the save file and turns each index into a club pointer, or null for minus one. | high | opus |  |
| 0x63e580 | 203 | `ItaCCup::set_predicted_positions` | thiscall(ItaCCup* this) ret 0 | Sorts the entrants by strength and sets each club's expected final position in the stats from the knockout rounds and the group places. | high | opus |  |
| 0x63e7f0 | 75 | `ItaCCup::set_club_progress` | thiscall(ItaCCup* this, Club* club, char stage, char current, char best, char worst) ret 0x14 | Maps group stage progress codes to final position codes and stores the current, best and worst progress in the club's stats entry. | high | opus |  |
