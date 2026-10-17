# hol_cup.cpp: 19 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5f3450 | 107 (+2 unwind) | `HolCup::HolCup` | thiscall(HolCup* this, short year, Nation* owner) ret 8, returns this | Constructs the Dutch cup on the League base, installs vtable 0x96b7b8 and, when no temp file loads, sets up 20 stage slots and the rules. | high | opus |  |
| 0x5f35e0 | 11 | `HolCup::`scalar deleting destructor'` | thiscall(HolCup* this, unsigned flags) ret 4, returns this | Runs the HolCup destructor and frees the object when the flags ask for it. | high | opus |  |
| 0x5f3600 | 66 (+1 unwind) | `HolCup::~HolCup` | thiscall(HolCup* this) ret 0 | Destroys the Dutch cup by freeing its table, schedule, entrant list, stage objects and stats object, then runs the League destructor. | high | opus |  |
| 0x5f36e0 | 389 | `HolCup::create_schedule` | thiscall(HolCup* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns schedule pointer | Builds the round schedule for a stage: three group dates for stages 0 to 18 and six knockout rounds for stage 19. | high | opus |  |
| 0x5f3c50 | 98 | `HolCup::build_fate_news_text` | thiscall(HolCup* this, int club_index, char fate, char stage, ...) ret 0x28 | Writes the news text for a club's fate: group qualification or exit in stages 0 to 18, tie result or final outcome in stage 19. | high | opus |  |
| 0x5f3d70 | 71 | `HolCup::create_group_table` | thiscall(HolCup* this) ret 0, returns 1 or 0 | Sets the cup's own group to four clubs, builds its table from the first four entrants and sends the group draw news. | medium | opus |  |
| 0x5f3e70 | 38 | `HolCup::set_up_rules` | thiscall(HolCup* this) ret 0, returns 1 | Sets the points, tiebreak and squad rules and the prize value of the cup, then creates the main schedule. | high | opus |  |
| 0x5f3f00 | 4 | `HolCup::record_season_honours` | thiscall(HolCup* this) ret 0, tail call | Passes the season honours call on to the knockout stage object in stage slot 19. | high | opus |  |
| 0x5f3f10 | 86 | `HolCup::start_new_season` | thiscall(HolCup* this) ret 0 | Frees last season's table, schedule, entrants and stages, archives the stats, moves the year on and sets the rules again. | high | opus |  |
| 0x5f4020 | 113 | `HolCup::update_for_date` | thiscall(HolCup* this, Date* today, int full_update) ret 8, returns int | On the first full update of the season, selects entrants, builds the main group and creates the 19 group stages, then runs the League update. | high | opus |  |
| 0x5f4190 | 40 | `HolCup::advance_stage` | thiscall(HolCup* this) ret 0 | Moves the current stage on and builds the knockout stage when the stage reaches 19, or reports an error past the last stage. | high | opus |  |
| 0x5f4220 | 183 (+1 unwind) | `HolCup::create_group_stage` | thiscall(HolCup* this, int stage) ret 4, returns 1 or 0 | Moves the next entrants into a new League_Stage group for one stage, with three clubs in stage 18, and sends the group draw news. | high | opus |  |
| 0x5f4480 | 283 (+1 unwind) | `HolCup::create_knockout_stage` | thiscall(HolCup* this) ret 0 | Pairs the twenty group winners with group runners-up at random, adds six seeded entrants and creates the stage 19 knockout and its first draw. | high | opus |  |
| 0x5f4820 | 399 | `HolCup::select_entrants` | thiscall(HolCup* this) ret 0, returns 1 or 0 | Fills an 86-slot entrant list with Dutch league and amateur clubs, removes duplicates, shuffles them in pots of eight and fills any gaps. | high | opus |  |
| 0x5f4d40 | 122 | `HolCup::update_staff_records_for_status` | thiscall(HolCup* this, Club* club, char status, char stage, int arg4, Fixture* fixture, int arg6) ret 0x18 | Adds staff history records for qualification or group exit in stages 0 to 18, and knock-out, progress, win or runner-up in stage 19. | high | opus |  |
| 0x5f4e90 | 151 | `HolCup::load_extra_data` | thiscall(HolCup* this, FILE* file) ret 4, returns 1 or 0 | Reads the entrant count and club indices from the save file and turns each index back into a club pointer. | high | opus |  |
| 0x5f5070 | 67 | `HolCup::save_extra_data` | thiscall(HolCup* this, FILE* file) ret 4 | Writes the entrant count and the entrants as club indices to the save file, then turns the indices back into club pointers. | high | opus |  |
| 0x5f5120 | 203 | `HolCup::set_predicted_positions` | thiscall(HolCup* this) ret 0 | Sorts the entrants by reputation and gives them predicted final positions by knockout round, then by groups of twenty. | high | opus |  |
| 0x5f5390 | 65 | `HolCup::set_club_progress` | thiscall(HolCup* this, Club* club, char stage, byte code1, byte code2, byte code3) ret 0x14, this not used | Maps group stage progress codes to cup round codes and stores the three progress fields on the club's stats entry. | high | opus |  |
