# hol_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5f8820 | 126 (+2 unwind) | `HolSuper::HolSuper` | thiscall(HolSuper* this, short year, void* comp_record), ret 8, returns this | Constructs the Dutch Super Cup on Cup and, when no saved data loads, picks its two clubs and builds its rounds, tie tree and stats. | high | opus |  |
| 0x5f89e0 | 11 | `HolSuper::`scalar deleting destructor'` | thiscall(HolSuper* this, unsigned flags), ret 4, returns this | Runs the Dutch Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5f8a00 | 62 (+1 unwind) | `HolSuper::~HolSuper` | thiscall(HolSuper* this), ret 0 | Destroys the Dutch Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x5f8ad0 | 98 | `HolSuper::create_round_table` | thiscall(HolSuper* this, char stage, short* round_count, short* extra, int* out), ret 0x10, returns Round* or null | Builds the one-round table of the Dutch Super Cup with its draw and match dates for two teams. | high | opus |  |
| 0x5f8c10 | 165 | `HolSuper::select_teams` | thiscall(HolSuper* this), ret 0, returns 1, 0 or -1 | Picks the Dutch First Division champion and the Dutch Cup winner, or the league runner-up when one club won both. | high | opus |  |
| 0x5f8e40 | 125 | `HolSuper::start_new_season` | thiscall(HolSuper* this), ret 0 | Clears the finished Dutch Super Cup, archives its stats, moves the year on and sets up the clubs and rounds of the next edition. | high | opus |  |
