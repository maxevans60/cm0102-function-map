# jap_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x665d70 | 129 (+2 unwind) | `JapSuper::JapSuper` | thiscall(JapSuper* this, short year, void* comp_record) ret 8, returns this | Constructs the Japanese Super Cup on Cup, loads it from disk or picks its two teams and builds the rounds, fixture tree, stats and ranking. | high | opus |  |
| 0x665f30 | 11 | `JapSuper::`scalar deleting destructor'` | thiscall(JapSuper* this, unsigned flags) ret 4, returns this | Runs the Japanese Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x665f50 | 62 (+1 unwind) | `JapSuper::~JapSuper` | thiscall(JapSuper* this) ret 0 | Destroys the Japanese Super Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x666020 | 98 | `JapSuper::create_round_table` | thiscall(JapSuper* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the one-round table of the Japanese Super Cup with its draw date, match date and final rules. | high | opus |  |
| 0x666160 | 263 | `JapSuper::select_teams` | thiscall(JapSuper* this) ret 0, returns 1, 0 on a missing club, -1 on allocation failure | Picks the J1 League champion and the Emperor's Cup winner for the Super Cup, using runners-up when a club is missing or appears twice. | high | opus |  |
| 0x6664e0 | 132 | `JapSuper::start_new_season` | thiscall(JapSuper* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and reselects the teams, rounds, fixture tree and ranking. | high | opus |  |
