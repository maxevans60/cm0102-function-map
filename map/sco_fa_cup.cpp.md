# sco_fa_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ed310 | 132 (+2 unwind) | `ScoFaCup::ScoFaCup` | thiscall(ScoFaCup* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Scottish Cup on Cup, then loads saved data or collects entrants, builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x7ed4e0 | 11 | `ScoFaCup::`scalar deleting destructor'` | thiscall(ScoFaCup* this, unsigned flags) ret 4, returns this | Runs the Scottish Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ed500 | 62 (+1 unwind) | `ScoFaCup::~ScoFaCup` | thiscall(ScoFaCup* this) ret 0 | Destroys the Scottish Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7ed5d0 | 325 | `ScoFaCup::create_round_table` | thiscall(ScoFaCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the seven-round table of the Scottish Cup with draw dates, match dates and round rules, from December to a late May final. | high | opus |  |
| 0x7edaf0 | 249 | `ScoFaCup::collect_entrants` | thiscall(ScoFaCup* this) ret 0, returns 1 when 50 entries fill, 0 when short, -1 on allocation failure | Fills the 50-entry entrant list with eight non-league Scottish clubs, the Second and Third Divisions shuffled, then the First and Premier Divisions. | high | opus |  |
| 0x7ede10 | 132 | `ScoFaCup::start_new_season` | thiscall(ScoFaCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
