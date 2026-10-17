# bel_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x420ef0 | 132 (+2 unwind) | `BelSuper::BelSuper` | thiscall(BelSuper* this, short year, void* comp_record) ret 8 | Constructs the Belgian Super Cup on Cup and, when no saved data loads, picks its two clubs and builds its rounds, tie tree and stats. | high | opus |  |
| 0x4210c0 | 11 | `BelSuper::`scalar deleting destructor'` | thiscall(BelSuper* this, unsigned flags) ret 4 | Runs the Belgian Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x4210e0 | 62 (+1 unwind) | `BelSuper::~BelSuper` | thiscall(BelSuper* this) ret 0 | Destroys the Belgian Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x4211b0 | 98 | `BelSuper::create_round_table` | thiscall(BelSuper* this, char stage, short* round_count, short* extra, int* out) ret 0x10 | Builds the one-round table of the Belgian Super Cup with its draw and match dates for two teams. | high | opus |  |
| 0x4212f0 | 173 | `BelSuper::select_teams` | thiscall(BelSuper* this) ret 0, returns 1, 0 or -1 | Picks the Belgian First Division champion and the Belgian Cup winner, or the league runner-up when one club won both, and swaps them in 2001. | high | opus |  |
| 0x421540 | 132 | `BelSuper::start_new_season` | thiscall(BelSuper* this) ret 0 | Clears the finished Belgian Super Cup, archives its stats, moves the year on and sets up the clubs and rounds of the next edition. | high | opus |  |
