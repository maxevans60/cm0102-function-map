# ire_lge_cup.cpp: 18 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x636dd0 | 175 (+2 unwind) | `IreLgeCup::IreLgeCup` | thiscall(IreLgeCup* this, short comp_id, int owner) ret 8 | Constructs the Irish League Cup on the League base, collects 26 entrants, builds the own table and fixtures and creates the seven group stages. | high | opus |  |
| 0x636f6c | 26 | `IreLgeCup::IreLgeCup_fragment_636f6c` | not a function entry: body fragment of 0x636dd0 sharing its stack frame, ret 8 | Repeats the assert message tail of the IreLgeCup constructor, read as a separate entry from inside that function. | high | opus |  |
| 0x637020 | 11 | `IreLgeCup::`scalar deleting destructor'` | thiscall(IreLgeCup* this, unsigned flags) ret 4, returns this | Runs the IreLgeCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x637040 | 66 (+1 unwind) | `IreLgeCup::~IreLgeCup` | thiscall(IreLgeCup* this) ret 0 | Destroys the Irish League Cup by freeing its table, schedule, entrant array, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x637120 | 270 | `IreLgeCup::create_schedule` | thiscall(IreLgeCup* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns schedule pointer | Builds the date template of a stage: three group matchdays for stages 0 to 6, or three knockout rounds for stage 7. | high | opus |  |
| 0x6374a0 | 98 | `IreLgeCup::build_fate_news_text` | thiscall(IreLgeCup* this, int club_index, char fate, char stage, ..., int full_sentence, ...) ret 0x28 | Writes a club's fate news, with a 'through to quarter finals' line for group qualifiers and cup tie text in the knockout stage. | high | opus |  |
| 0x6375c0 | 71 | `IreLgeCup::create_table` | thiscall(IreLgeCup* this) ret 0, returns 1 or 0 on allocation failure | Sets the own table to three clubs, allocates it, fills it with the first three entrants and sends the group draw news. | high | opus |  |
| 0x6376c0 | 37 | `IreLgeCup::set_up_rules` | thiscall(IreLgeCup* this) ret 0, returns 1 | Sets the points, tiebreak and promotion rule fields of the Irish League Cup and builds its season schedule. | high | opus |  |
| 0x637750 | 4 | `IreLgeCup::record_season_honours` | thiscall(IreLgeCup* this) ret 0, tail jump | Forwards the season honours call to the knockout stage held in the eighth stage slot. | high | opus |  |
| 0x637760 | 151 | `IreLgeCup::start_new_season` | thiscall(IreLgeCup* this) ret 0 | Frees last season's table, entrants and stages, then collects new entrants and rebuilds the rules, table, fixtures and seven group stages. | high | opus |  |
| 0x637930 | 40 | `IreLgeCup::advance_stage` | thiscall(IreLgeCup* this) ret 0 | Moves the current stage index on by one and creates the knockout stage when the index reaches stage 7. | high | opus |  |
| 0x6379c0 | 174 (+1 unwind) | `IreLgeCup::create_group_stage` | thiscall(IreLgeCup* this, int group) ret 4, returns 1 or 0 on failure | Takes the next unused entrants from the pool and builds a League_Stage group for the given group index. | high | opus |  |
| 0x637c00 | 147 (+1 unwind) | `IreLgeCup::create_knockout_stage` | thiscall(IreLgeCup* this) ret 0 | Collects the eight group winners and builds the knockout Cup_Stage in stage slot 7, then draws its first round. | high | opus |  |
| 0x637dd0 | 262 | `IreLgeCup::collect_entrants` | thiscall(IreLgeCup* this) ret 0, returns 1 or 0 on allocation failure | Fills a 26-entry pool with Irish clubs, placing them into regional buckets by reserve division or division, shuffling buckets and topping up empty places. | medium | opus |  |
| 0x638110 | 122 | `IreLgeCup::update_staff_records_for_status` | thiscall(IreLgeCup* this, Club* club, char status, char stage, int arg, Fixture* fixture, int arg2) ret 0x18 | Adds staff history records for group qualification or failure and for knockout exits, wins and runner-up places. | high | opus |  |
| 0x638260 | 141 | `IreLgeCup::load_extra_data` | thiscall(IreLgeCup* this, FILE* file) ret 4, returns 1 or 0 on read failure | Reads the entrant count and club ids from the save file and turns each id back into a club pointer. | high | opus |  |
| 0x638420 | 203 | `IreLgeCup::set_predicted_positions` | thiscall(IreLgeCup* this) ret 0 | Sorts the entrants by reputation and stores predicted final positions in Comp_Stats by the round each club is expected to reach. | high | opus |  |
| 0x638690 | 75 | `IreLgeCup::set_club_progress` | thiscall(IreLgeCup* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, mapping group places 1 to 4 to codes 1, 9, 17 and 25. | high | opus |  |
