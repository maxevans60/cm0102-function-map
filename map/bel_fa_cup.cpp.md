# bel_fa_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x41d050 | 133 (+2 unwind) | `BelFaCup::BelFaCup` | thiscall(BelFaCup* this, short comp_id, int nation) ret 8 | Constructs the Belgian cup, loads it from disk or collects entrants and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x41d220 | 11 | `BelFaCup::`scalar deleting destructor'` | thiscall(BelFaCup* this, unsigned flags) ret 4, returns this | Runs the Belgian cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x41d240 | 62 (+1 unwind) | `BelFaCup::~BelFaCup` | thiscall(BelFaCup* this) ret 0 | Destroys the Belgian cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x41d310 | 361 | `BelFaCup::create_round_table` | thiscall(BelFaCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the eight-round table of the Belgian cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x41d8d0 | 208 | `BelFaCup::collect_entrants` | thiscall(BelFaCup* this) ret 0, returns 1 when 112 entries fill, 0 when short, -1 on allocation failure | Fills the 112-entry six-byte entrant list with Belgian clubs, the top divisions shuffled first and lower divisions entering at earlier rounds. | high | opus |  |
| 0x41db90 | 132 | `BelFaCup::start_new_season` | thiscall(BelFaCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
