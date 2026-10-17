# usa_open_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x90aeb0 | 130 (+2 unwind) | `UsaOpenCup::UsaOpenCup` | thiscall(UsaOpenCup* this, short season_year, CompRecord* comp) ret 8, returns this | Constructs the US Open Cup on Cup, loads saved data or collects entrants, and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x90b080 | 11 | `UsaOpenCup::`scalar deleting destructor'` | thiscall(UsaOpenCup* this, unsigned flags) ret 4, returns this | Runs the US Open Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x90b0a0 | 62 (+1 unwind) | `UsaOpenCup::~UsaOpenCup` | thiscall(UsaOpenCup* this) ret 0 | Destroys the US Open Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x90b170 | 249 | `UsaOpenCup::create_round_table` | thiscall(UsaOpenCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the five-round table of the US Open Cup for stage -1 with draw dates, match dates and round rules, starting with 32 teams. | high | opus |  |
| 0x90b530 | 176 | `UsaOpenCup::collect_entrants` | thiscall(UsaOpenCup* this) ret 0, returns 1, or -1 on allocation failure | Fills the 32-entry entrant list with ten shuffled clubs from each of two US lower competitions, then adds the clubs of the competition at 0x9cf590. | medium | opus | arg-usa.md |
| 0x90b790 | 132 | `UsaOpenCup::start_new_season` | thiscall(UsaOpenCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus | 2026-10-16-research-name-check.md |
