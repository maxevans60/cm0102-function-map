# pol_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7c7d80 | 132 (+2 unwind) | `PolCup::PolCup` | thiscall(PolCup* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Polish FA Cup on Cup, then loads saved data or collects entrants and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x7c7f50 | 11 | `PolCup::`scalar deleting destructor'` | thiscall(PolCup* this, unsigned flags) ret 4, returns this | Runs the Polish FA Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7c7f70 | 62 (+1 unwind) | `PolCup::~PolCup` | thiscall(PolCup* this) ret 0 | Destroys the Polish FA Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7c8040 | 325 | `PolCup::create_round_table` | thiscall(PolCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the seven-round table of the Polish FA Cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x7c8550 | 253 | `PolCup::collect_entrants` | thiscall(PolCup* this) ret 0, returns 1 on success and -1 on allocation failure | Fills the 52-entry entrant list with Polish Second Division, Lower Division and First Division clubs, each tagged with its entry round. | high | opus |  |
| 0x7c88a0 | 132 | `PolCup::start_new_season` | thiscall(PolCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus |  |
| 0x7c8a50 | 16 | `PolCup::set_up_rounds` | thiscall(PolCup* this) ret 0, returns 1 | Sets the Polish FA Cup prize fund to 600000 and builds the round table for stage -1. | high | opus |  |
