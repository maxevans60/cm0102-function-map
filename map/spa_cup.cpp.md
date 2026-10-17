# spa_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x84cf50 | 134 (+2 unwind) | `SpaCup::SpaCup` | thiscall(SpaCup* this, short season_year, int comp_record) ret 8, returns this | Constructs the Spanish cup. Without saved data it allocates 83 entries, sets a 1000000 prize fund and builds rounds, fixture tree and stats. | high | opus |  |
| 0x84d130 | 11 | `SpaCup::`scalar deleting destructor'` | thiscall(SpaCup* this, unsigned flags) ret 4, returns this | Runs the SpaCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x84d150 | 62 (+1 unwind) | `SpaCup::~SpaCup` | thiscall(SpaCup* this) ret 0 | Destroys the Spanish cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x84d220 | 324 | `SpaCup::create_round_table` | thiscall(SpaCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the seven-round Spanish cup table with draw dates, match dates, round codes and entry counts for stage -1. | high | opus |  |
| 0x84d740 | 136 | `SpaCup::update_for_date` | thiscall(SpaCup* this, Date* today, int phase) ret 8 | On the first update of the cup year it collects entrants and rebuilds rounds, tree and rankings, then runs the base Cup update. | high | opus |  |
| 0x84d910 | 473 | `SpaCup::collect_entrants` | thiscall(SpaCup* this) ret 0, returns 1 when done, 0 or -1 on allocation failure | Fills the 83-entry Spanish cup list with lower division clubs first, then Second Division, First Division and European clubs last. | high | opus |  |
| 0x84df70 | 138 | `SpaCup::start_new_season` | thiscall(SpaCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entry list, rounds, tree and rankings. | high | opus |  |
