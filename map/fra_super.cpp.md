# fra_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5bf320 | 126 (+2 unwind) | `FraSuper::FraSuper` | thiscall(FraSuper* this, short year, void* comp_record), ret 8 | Constructs the French Super Cup on Cup and, when no saved data loads, picks its two clubs and builds its rounds, tie tree and stats. | high | opus |  |
| 0x5bf4e0 | 11 | `FraSuper::`scalar deleting destructor'` | thiscall(FraSuper* this, unsigned flags), ret 4, returns this | Runs the French Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bf500 | 62 (+1 unwind) | `FraSuper::~FraSuper` | thiscall(FraSuper* this), ret 0 | Destroys the French Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x5bf5d0 | 121 | `FraSuper::create_round_table` | thiscall(FraSuper* this, char stage, short* round_count, short* extra, int* out), ret 0x10, returns Round* or null | Builds the one-round table of the French Super Cup with its draw and match dates for two teams and a random match weekday flag. | high | opus |  |
| 0x5bf770 | 165 | `FraSuper::select_teams` | thiscall(FraSuper* this), ret 0, returns 1, 0 or -1 | Picks the French First Division champion and the French Cup winner, or the league runner-up when one club won both. | high | opus |  |
| 0x5bf9a0 | 125 | `FraSuper::start_new_season` | thiscall(FraSuper* this), ret 0 | Clears the finished French Super Cup, archives its stats, moves the year on and sets up the clubs and rounds of the next edition. | high | opus |  |
