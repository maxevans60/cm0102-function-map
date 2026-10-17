# jap_j1.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x662b30 | 160 (+2 unwind) | `JapJ1::JapJ1` | thiscall(JapJ1* this, short id, int parent) ret 8, returns this | Constructs the J1 League on League, then loads its saved state or sets the rules, builds the table and fixtures and creates its statistics. | high | opus |  |
| 0x662d50 | 11 | `JapJ1::`scalar deleting destructor'` | thiscall(JapJ1* this, unsigned flags) ret 4, returns this | Runs the J1 League destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x662d70 | 58 (+1 unwind) | `JapJ1::~JapJ1` | thiscall(JapJ1* this) ret 0 | Destroys the J1 League by freeing its table, schedule, every stage object and the statistics, then runs the League destructor. | high | opus |  |
| 0x662e30 | 735 | `JapJ1::create_schedule` | thiscall(JapJ1* this, char stage, short* entry_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 30 matchday dates of the two league stages, or the one-round championship final for stage 2. | high | opus |  |
| 0x6634e0 | 101 | `JapJ1::create_table` | thiscall(JapJ1* this) ret 0, returns 1 on success | Sets the team count to 16, places every J1 club in the league table and sets and pays the prize fund. | high | opus |  |
| 0x663620 | 42 | `JapJ1::set_up_rules` | thiscall(JapJ1* this) ret 0, returns 1 | Sets the points, tiebreak and match rules of the J1 League, names J2 as the relegation division and builds the schedule. | high | opus |  |
| 0x6636d0 | 191 | `JapJ1::start_new_season` | thiscall(JapJ1* this) ret 0 | Frees last season's table, schedule and stages, archives the statistics, advances the year and rebuilds the rules, table and fixtures. | high | opus |  |
| 0x663940 | 49 | `JapJ1::add_result` | thiscall(JapJ1* this, Fixture* match, int update_stats) ret 8, returns 1 | Adds a match to the full table, then to the first or second stage table by matchday, creating the second stage when it starts. | high | opus |  |
| 0x6639c0 | 40 | `JapJ1::advance_stage` | thiscall(JapJ1* this) ret 0 | Moves the stage counter on and creates the championship final when stage 2 begins, or reports an error past the last stage. | high | opus |  |
| 0x663a50 | 136 (+1 unwind) | `JapJ1::create_championship_final_stage` | thiscall(JapJ1* this) ret 0 | Builds the two-club championship final stage from the winners of the first and second stages and sets up its round. | high | opus |  |
| 0x663c20 | 125 (+1 unwind) | `JapJ1::create_half_season_stage` | thiscall(JapJ1* this, char stage_index) ret 4 | Builds a League_Stage for the first or second half of the season from all J1 clubs and stores it in the stage table. | high | opus |  |
| 0x663db0 | 258 | `JapJ1::update_staff_records_for_status` | thiscall(JapJ1* this, Club* club, char status, char stage, char* changed, int unused) ret 0x18 | Adds stage winner, champion or final loser records for a club by stage and status and marks its table row progress code. | high | opus |  |
| 0x6640a0 | 259 | `JapJ1::build_fate_news_text` | thiscall(JapJ1* this, int club_index, int status, char stage, int a5, int a6, int a7, int stage_won, int a9, int long_text, int a11) ret 0x28 | Writes the news for a club that wins a stage, wins the J1 League or loses its final, and passes other fates to Comp. | high | opus |  |
| 0x664390 | 46 | `JapJ1::record_season_honours` | thiscall(JapJ1* this) ret 0 | Records the season history with the winner of the first stage when only two stages ran, or hands the task to the final stage. | high | opus |  |
| 0x664400 | 69 | `JapJ1::set_club_progress` | thiscall(JapJ1* this, Club* club, char stage, char current, char best, char last) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, capping middle codes at 2 and 5 during the full season stage. | high | opus |  |
