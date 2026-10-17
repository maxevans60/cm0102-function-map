# wel_lge_cup.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x925e90 | 175 (+2 unwind) | `WelLgeCup::WelLgeCup` | thiscall(WelLgeCup* this, short comp_id, int owner) ret 8, returns this | Constructs the Welsh League Cup on League, then loads saved data or collects 18 entrants and builds the table, fixtures and five group stages. | high | opus |  |
| 0x9260e0 | 11 | `WelLgeCup::`scalar deleting destructor'` | thiscall(WelLgeCup* this, unsigned flags) ret 4, returns this | Runs the WelLgeCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x926100 | 66 (+1 unwind) | `WelLgeCup::~WelLgeCup` | thiscall(WelLgeCup* this) ret 0 | Destroys the Welsh League Cup by freeing its table, schedule, entrant array, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x9261e0 | 330 | `WelLgeCup::create_schedule` | thiscall(WelLgeCup* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns schedule pointer | Builds a stage's date template, with six group matchdays from late August for stages 0 to 4 or three knockout rounds for stage 5. | high | opus |  |
| 0x9265e0 | 98 | `WelLgeCup::build_fate_news_text` | thiscall(WelLgeCup* this, int club_index, char fate, char stage, ..., int full_sentence, ...) ret 0x28 | Writes a club's fate news, with a 'through to quarter finals' line for group qualifiers and cup tie text in the knockout stage. | high | opus |  |
| 0x926700 | 72 | `WelLgeCup::create_table` | thiscall(WelLgeCup* this) ret 0, returns 1 or 0 on allocation failure | Sets the own table to three clubs, allocates it, fills it with the first entrant of each seeding row and sends the group draw news. | high | opus |  |
| 0x926800 | 38 | `WelLgeCup::set_up_rules` | thiscall(WelLgeCup* this) ret 0, returns 1 | Sets the points, tiebreak and promotion rule fields of the Welsh League Cup, a prize fund of 100000, and builds its season schedule. | high | opus |  |
| 0x926890 | 4 | `WelLgeCup::record_season_honours` | thiscall(WelLgeCup* this) ret 0 (tail jump) | Forwards the season honours call to the knockout stage held in the sixth stage slot. | high | opus |  |
| 0x9268a0 | 151 | `WelLgeCup::start_new_season` | thiscall(WelLgeCup* this) ret 0 | Frees last season's table, entrants and stages, archives the stats, then collects new entrants and rebuilds the rules, table, fixtures and five groups. | high | opus |  |
| 0x926a70 | 40 | `WelLgeCup::advance_stage` | thiscall(WelLgeCup* this) ret 0 | Moves the current stage index on by one and creates the knockout stage when the index reaches stage 5. | high | opus |  |
| 0x926b00 | 157 (+1 unwind) | `WelLgeCup::create_group_stage` | thiscall(WelLgeCup* this, int group) ret 4, returns 1 or 0 on failure | Takes three entrants from the pool column of the given group and builds a three-club League_Stage group in that stage slot. | high | opus |  |
| 0x926d00 | 244 (+2 unwind) | `WelLgeCup::create_knockout_stage` | thiscall(WelLgeCup* this) ret 0 | Builds the eight-club knockout Cup_Stage from the six group winners and the two best runners-up, then draws its first round. | high | opus |  |
| 0x927010 | 135 | `WelLgeCup::collect_entrants` | thiscall(WelLgeCup* this) ret 0, returns 1 or 0 on allocation failure | Fills an 18-entry pool with Welsh league clubs, sorts them by reputation and shuffles each block of three for the group draw. | high | opus |  |
| 0x9271e0 | 122 | `WelLgeCup::update_staff_records_for_status` | thiscall(WelLgeCup* this, Club* club, char status, char stage, int arg, Fixture* fixture, int arg2) ret 0x18 | Adds staff history records for group qualification or failure and for knockout exits, wins and runner-up places. | high | opus |  |
| 0x927330 | 141 | `WelLgeCup::load_extra_data` | thiscall(WelLgeCup* this, FILE* file) ret 4, returns 1 or 0 on read failure | Reads the entrant count and club ids from the save file and turns each id back into a club pointer. | high | opus |  |
| 0x9274f0 | 203 | `WelLgeCup::set_predicted_positions` | thiscall(WelLgeCup* this) ret 0 | Sorts the entrants by reputation and stores predicted final positions in Comp_Stats by the knockout round each club is expected to reach. | high | opus |  |
| 0x927760 | 56 | `WelLgeCup::set_club_progress` | thiscall(WelLgeCup* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, mapping group places 1 and 2 to code 1 and place 3 to code 9. | high | opus |  |
