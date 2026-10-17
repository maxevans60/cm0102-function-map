# sco_chal_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ec980 | 132 (+2 unwind) | `ScoChalCup::ScoChalCup` | thiscall(ScoChalCup* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Scottish Challenge Cup on Cup, then loads saved data or collects entrants, builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x7ecb50 | 11 | `ScoChalCup::`scalar deleting destructor'` | thiscall(ScoChalCup* this, unsigned flags) ret 4, returns this | Runs the Scottish Challenge Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ecb70 | 62 (+1 unwind) | `ScoChalCup::~ScoChalCup` | thiscall(ScoChalCup* this) ret 0 | Destroys the Scottish Challenge Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7ecc40 | 249 | `ScoChalCup::create_round_table` | thiscall(ScoChalCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the five-round table of the Scottish Challenge Cup with draw dates, match dates and round rules for stage -1. | high | opus |  |
| 0x7ed010 | 89 | `ScoChalCup::collect_entrants` | thiscall(ScoChalCup* this) ret 0, returns 1 when 30 entries fill, 0 when short, -1 on allocation failure | Fills the 30-entry six-byte entrant list with the clubs of the Scottish First, Second and Third Divisions. | high | opus |  |
| 0x7ed130 | 132 | `ScoChalCup::start_new_season` | thiscall(ScoChalCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
| 0x7ed2e0 | 16 | `ScoChalCup::set_up_rounds` | thiscall(ScoChalCup* this) ret 0, returns 1 | Sets a prize fund of 200000 and builds the round table of the Scottish Challenge Cup through create_round_table for stage -1. | high | opus |  |
