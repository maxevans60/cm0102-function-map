# aus_nsl.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x410e90 | 160 (+2 unwind) | `AusNsl::AusNsl` | thiscall(AusNsl* this, short year, int comp_id) ret 8, returns this | Builds the Australian National Soccer League on top of League, sets its rules, fills its 13-club table, makes the fixtures and the Comp_Stats object. | high | opus |  |
| 0x4110b0 | 2 | `AusNsl::get_table_layout_type` | thiscall(AusNsl* this) returns char 3, ret 0 | Returns 3 as the table layout code, so the standings screens use a column set unlike the Comp default of 2. | high | opus |  |
| 0x4110c0 | 11 | `AusNsl::`scalar deleting destructor'` | thiscall(AusNsl* this, unsigned flags) ret 4, returns this | Runs the AusNsl destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x4110e0 | 60 (+1 unwind) | `AusNsl::~AusNsl` | thiscall(AusNsl* this) ret 0 | Destroys the Australian league by freeing its table, schedule, stage objects and stats, then runs the League destructor. | high | opus |  |
| 0x4111a0 | 850 | `AusNsl::create_schedule` | thiscall(AusNsl* this, char stage, short* round_count, short* comp_code, int* is_league) ret 0x10, returns schedule buffer | Builds the date template of one stage: 24 rounds for the regular season, 10 rounds for the finals series or one grand final tie. | high | opus |  |
| 0x411980 | 59 | `AusNsl::update_staff_records_for_status` | thiscall(AusNsl* this, Club* club, char status, char stage, ...) ret 0x18, returns 0 or -1 | Writes the staff history record for a club's status: qualified for the finals series or grand final, failed to qualify, or league champions. | high | opus |  |
| 0x411a30 | 106 | `AusNsl::build_fate_news_text` | thiscall(AusNsl* this, int club_index, int fate, char stage, int a4, int a5, int a6, int a7, int a8, int full_sentence, int a10) ret 0x28 | Writes the news text for a club's fate in the NSL, from reaching the playoff phase or the final to winning or losing the final. | high | opus |  |
| 0x411b70 | 113 | `AusNsl::create_table` | thiscall(AusNsl* this) ret 0, returns 1 or 0 | Sets the team count to 13, allocates the league table and fills it with every club whose nation is Australia. | high | opus |  |
| 0x411ce0 | 38 | `AusNsl::set_up_rules` | thiscall(AusNsl* this) ret 0, returns 1 | Sets the NSL rule fields, such as the substitute counts, and builds the regular season schedule. | high | opus |  |
| 0x411d90 | 35 | `AusNsl::record_season_honours` | thiscall(AusNsl* this) ret 0 | Records the grand final winner, runner-up and regular season leader in the competition history. | high | opus |  |
| 0x411de0 | 125 | `AusNsl::start_new_season` | thiscall(AusNsl* this) ret 0 | Archives last season, increments the year and rebuilds the rules, table and fixtures of the Australian league for a new season. | high | opus |  |
| 0x411f70 | 45 | `AusNsl::advance_stage` | thiscall(AusNsl* this) ret 0 | Moves the NSL to its next stage and builds the finals series stage or the grand final stage. | high | opus |  |
| 0x412010 | 130 (+1 unwind) | `AusNsl::create_finals_series_stage` | thiscall(AusNsl* this) ret 0, returns bool | Builds a six-club League_Stage from the top six of the regular season table and sends the draw news for the finals series. | high | opus |  |
| 0x412070 | 104 | `AusNsl::create_finals_series_stage_fragment_412070` | body fragment inside 0x412010, shares its frame, ret 0 | Inner entry of AusNsl::create_finals_series_stage that starts at the schedule call and builds and stores the six-club stage. | medium | opus |  |
| 0x4121c0 | 133 (+1 unwind) | `AusNsl::create_grand_final_stage` | thiscall(AusNsl* this) ret 0 | Builds a two-club Cup_Stage from the top two of the finals series table and sets up the grand final round. | high | opus |  |
| 0x412380 | 101 | `AusNsl::set_club_progress` | thiscall(AusNsl* this, Club* club, char stage, char result, char position, char finish) ret 0x14, this unused | Writes a club's stage result, position and finish code into its Comp_Stats entry, mapping finals series and regular season codes onto knockout codes. | high | opus |  |
| 0x4124e0 | 27 | `AusNsl::set_fixture_substitutes` | thiscall(AusNsl* this, Fixture* fixture) ret 4 | Packs the substitute counts into a fixture's substitutes word, with five named and three used for fixtures of a stage. | high | opus |  |
