# pol_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7cc920 | 128 (+2 unwind) | `PolSuper::PolSuper` | thiscall(PolSuper* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Polish Super Cup on Cup and, when no saved data loads, picks its two clubs and builds its rounds, tie tree and stats. | high | opus |  |
| 0x7ccae0 | 11 | `PolSuper::`scalar deleting destructor'` | thiscall(PolSuper* this, unsigned flags) ret 4, returns this | Runs the Polish Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ccb00 | 62 (+1 unwind) | `PolSuper::~PolSuper` | thiscall(PolSuper* this) ret 0 | Destroys the Polish Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7ccbd0 | 99 | `PolSuper::create_round_table` | thiscall(PolSuper* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* or null | Builds the one-round table of the Polish Super Cup with its draw and match dates for two teams and no prize money. | high | opus |  |
| 0x7ccd10 | 188 | `PolSuper::select_teams` | thiscall(PolSuper* this) ret 0, returns 1, 0 or -1 | Picks the Polish First Division champion and the Polish Cup winner, or the cup runner-up when one club won both. | high | opus |  |
| 0x7ccf90 | 125 | `PolSuper::start_new_season` | thiscall(PolSuper* this) ret 0 | Clears the finished Polish Super Cup, archives its stats, moves the year on and sets up the clubs and rounds of the next edition. | high | opus |  |
