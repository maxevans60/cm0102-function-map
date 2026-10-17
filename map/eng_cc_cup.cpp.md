# eng_cc_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x56c2a0 | 133 (+2 unwind) | `EngCcCup::EngCcCup` | thiscall(EngCcCup* this, short season_year, int parent) ret 8 | Constructs the English League Cup, loads it from disk or allocates the 92-club entrant list and builds the round table, fixture tree and stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x56c480 | 11 | `EngCcCup::`scalar deleting destructor'` | thiscall(EngCcCup* this, unsigned flags) ret 4 | Runs the EngCcCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x56c4a0 | 62 (+1 unwind) | `EngCcCup::~EngCcCup` | thiscall(EngCcCup* this) ret 0 | Destroys the League Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x56c570 | 346 | `EngCcCup::create_round_table` | thiscall(EngCcCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the seven-round League Cup table with draw dates, match dates and round rules, sizing the early rounds by the European byes count. | high | opus |  |
| 0x56caf0 | 136 | `EngCcCup::update_for_date` | thiscall(EngCcCup* this, Date* today, int phase) ret 8 | Collects the entrants and builds rounds, fixture tree and ranking once the season year starts, then runs the Cup daily update. | high | opus |  |
| 0x56ccc0 | 341 | `EngCcCup::collect_entrants` | thiscall(EngCcCup* this) ret 0, returns 1 when 92 entries fill, 0 when short, -1 on allocation failure | Fills the 92-entry League Cup entrant list from the four league divisions, seeding the clubs in Europe and counting them as byes. | high | opus |  |
| 0x56d130 | 131 | `EngCcCup::start_new_season` | thiscall(EngCcCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and allocates a fresh entrant list, round table and fixture tree. | high | opus |  |
| 0x56d2e0 | 42 | `EngCcCup::load_extra_data` | thiscall(EngCcCup* this, FILE* file) ret 4, returns 1 or 0 | Reads the European byes count byte at +0xb2 from the save file and reports an error when the read fails. | high | opus |  |
