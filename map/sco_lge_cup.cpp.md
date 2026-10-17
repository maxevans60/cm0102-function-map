# sco_lge_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ef9e0 | 135 (+2 unwind) | `ScoLgeCup::ScoLgeCup` | thiscall(ScoLgeCup* this, short season_year, int parent) ret 8, returns this | Constructs the Scottish League Cup, loads it from disk or allocates the 40-club entrant list and builds rounds, fixture tree and stats. | high | opus |  |
| 0x7efbc0 | 11 | `ScoLgeCup::`scalar deleting destructor'` | thiscall(ScoLgeCup* this, unsigned flags) ret 4, returns this | Runs the ScoLgeCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7efbe0 | 62 (+1 unwind) | `ScoLgeCup::~ScoLgeCup` | thiscall(ScoLgeCup* this) ret 0 | Destroys the Scottish League Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7efcb0 | 348 | `ScoLgeCup::create_round_table` | thiscall(ScoLgeCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the six-round Scottish League Cup table with draw dates, match dates and round rules, sizing early rounds by the European byes count. | high | opus |  |
| 0x7f0230 | 136 | `ScoLgeCup::update_for_date` | thiscall(ScoLgeCup* this, Date* today, int phase) ret 8 | Collects the entrants and builds rounds, fixture tree and ranking once the season year starts, then runs the Cup daily update. | high | opus |  |
| 0x7f0400 | 369 | `ScoLgeCup::collect_entrants` | thiscall(ScoLgeCup* this) ret 0, returns 1 when the list fills, 0 when short, -1 on allocation failure | Fills the 40-entry, later 42-entry, League Cup entrant list from the four Scottish divisions, seeding clubs in Europe and counting them as byes. | high | opus |  |
| 0x7f0930 | 130 | `ScoLgeCup::start_new_season` | thiscall(ScoLgeCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and allocates a fresh entrant list, round table and fixture tree. | high | opus |  |
| 0x7f0ae0 | 42 | `ScoLgeCup::load_extra_data` | thiscall(ScoLgeCup* this, FILE* file) ret 4, returns 1 or 0 | Reads the European byes count byte at +0xb2 from the save file and reports an error when the read fails. | high | opus |  |
