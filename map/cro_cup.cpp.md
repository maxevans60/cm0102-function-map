# cro_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x517480 | 132 (+2 unwind) | `CroCup::CroCup` | thiscall(CroCup* this, short season_year, int parent) ret 8 | Constructs the Croatian cup on Cup, loads it from disk or collects entrants and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x517650 | 11 | `CroCup::`scalar deleting destructor'` | thiscall(CroCup* this, unsigned flags) ret 4 | Runs the CroCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x517670 | 62 (+1 unwind) | `CroCup::~CroCup` | thiscall(CroCup* this) ret 0 | Destroys the Croatian cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x517740 | 289 | `CroCup::create_round_table` | thiscall(CroCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10 | Allocates and fills the six-round table of the Croatian cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x517bb0 | 129 | `CroCup::collect_entrants` | thiscall(CroCup* this) ret 0, returns 1 on success or -1 | Fills the 48-entry six-byte entrant list with the second division clubs and a random seed, then adds the top division clubs. | high | opus |  |
| 0x517d60 | 132 | `CroCup::start_new_season` | thiscall(CroCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
