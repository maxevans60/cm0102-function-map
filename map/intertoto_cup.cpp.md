# intertoto_cup.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x632fb0 | 139 (+2 unwind) | `IntertotoCup::IntertotoCup` | thiscall(IntertotoCup* this, short comp_id, int owner), returns this, ret 8 | Runs the Cup constructor, installs vtable 0x96bb8c, loads the saved cup or collects the 60 entrants and builds rounds, tree and statistics. | high | opus |  |
| 0x6331a0 | 11 | `IntertotoCup::`scalar deleting destructor'` | thiscall(IntertotoCup* this, unsigned flags), ret 4 | Runs the IntertotoCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x6331c0 | 62 (+1 unwind) | `IntertotoCup::~IntertotoCup` | thiscall(IntertotoCup* this), ret 0 | Restores the vtable, frees the entrant list, round table and stage arrays and the statistics, then runs the Cup destructor. | high | opus |  |
| 0x633290 | 42 | `IntertotoCup::process_fixture` | thiscall(IntertotoCup* this, Fixture* fixture, int arg), ret 8 | Adds UEFA coefficient points to the nations of both clubs from the fixture result, then runs the base cup fixture processing. | high | opus | 2026-10-16-sweep-europe.md |
| 0x633300 | 249 | `IntertotoCup::create_round_table` | thiscall(IntertotoCup* this, char stage, short* round_count, short* extra, int* out), returns round table, ret 0x10 | Allocates the five-round Intertoto Cup table and sets each round's draw date, match dates, ties and qualifiers. | high | opus | 2026-10-16-sweep-europe.md |
| 0x6336c0 | 182 | `IntertotoCup::collect_entrants` | thiscall(IntertotoCup* this), returns 1, 0 or -1, ret 0 | Collects the 60 clubs entered for the Intertoto Cup into the six-byte entrant list and sorts them by seed. | high | opus | 2026-10-16-sweep-europe.md |
| 0x633920 | 141 | `IntertotoCup::start_new_season` | thiscall(IntertotoCup* this), ret 0 | Frees the season data, archives the statistics, advances the year, then collects new entrants and rebuilds rounds, stages and the first round. | high | opus |  |
| 0x633af0 | 97 | `IntertotoCup::build_fate_news_text` | thiscall(IntertotoCup* this, int club_index, char fate, ..., int cup_result, ...) ret 0x28 | Writes the news text that a club qualifies for the UEFA Cup, and passes other fates to the base text builder. | high | opus |  |
| 0x633c10 | 105 | `IntertotoCup::update_staff_records_for_status` | thiscall(IntertotoCup* this, Club* club, char outcome, int arg3, int arg4, Fixture* fixture, int arg6), ret 0x18 | Records a club's Intertoto outcome in staff records and moves a qualified club into the UEFA Cup or clears an eliminated club's entry. | high | opus |  |
| 0x633d40 | 106 | `IntertotoCup::update_for_date` | thiscall(IntertotoCup* this, Date* today, int phase), ret 8 | When the cup ends, copies its winners into the last places of the UEFA Cup entrant list once, then runs the base daily update. | high | opus | 2026-10-16-sweep-europe.md |
| 0x633eb0 | 42 | `IntertotoCup::load_extra_data` | thiscall(IntertotoCup* this, FILE* file), returns 1 or 0, ret 4 | Reads the four-byte winners-passed flag of the Intertoto Cup from the save file. | high | opus |  |
| 0x633f50 | 9 | `IntertotoCup::save_extra_data` | thiscall(IntertotoCup* this, FILE* file), ret 4 | Writes the four-byte winners-passed flag of the Intertoto Cup to the save file. | high | opus |  |
| 0x633f70 | 102 | `IntertotoCup::collect_club_list` | thiscall(IntertotoCup* this, Club*** out_clubs, char active_only), returns club count as short, ret 8 | Returns a new array of the entrant club pointers, optionally only those whose state byte is 0 or 1. | high | opus |  |
