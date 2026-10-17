# jap_j_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x665380 | 132 (+2 unwind) | `JapJCup::JapJCup` | thiscall(JapJCup* this, short year, void* comp_record) ret 8, returns this | Constructs the Japanese J League Cup on Cup, loads it from disk or collects entrants and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x665550 | 11 | `JapJCup::`scalar deleting destructor'` | thiscall(JapJCup* this, unsigned flags) ret 4, returns this | Runs the J League Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x665570 | 62 (+1 unwind) | `JapJCup::~JapJCup` | thiscall(JapJCup* this) ret 0 | Destroys the J League Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x665640 | 249 | `JapJCup::create_round_table` | thiscall(JapJCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the five-round table of the J League Cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x665a00 | 136 | `JapJCup::collect_entrants` | thiscall(JapJCup* this) ret 0, returns 1 when 28 entries fill, 0 when short, -1 on allocation failure | Fills the 28-entry six-byte entrant list with the J2 clubs first, then the J1 clubs with a random seed, and sorts part of the list. | high | opus |  |
| 0x665bc0 | 132 | `JapJCup::start_new_season` | thiscall(JapJCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
