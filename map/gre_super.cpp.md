# gre_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5ec040 | 128 (+2 unwind) | `GreSuper::GreSuper` | thiscall(GreSuper* this, short year, void* comp_record) ret 8, returns this | Constructs the Greek Super Cup on Cup and, when no saved data loads, picks its two clubs and builds its rounds, tie tree and stats. | high | opus |  |
| 0x5ec200 | 11 | `GreSuper::`scalar deleting destructor'` | thiscall(GreSuper* this, unsigned flags) ret 4, returns this | Runs the Greek Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5ec220 | 62 (+1 unwind) | `GreSuper::~GreSuper` | thiscall(GreSuper* this) ret 0 | Destroys the Greek Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x5ec2f0 | 99 | `GreSuper::create_round_table` | thiscall(GreSuper* this, char stage, short* round_count, short* extra, int* out_flag) ret 0x10, returns round table pointer | Builds the one-round table of the Greek Super Cup with its draw and match dates for two teams. | high | opus |  |
| 0x5ec430 | 188 | `GreSuper::select_teams` | thiscall(GreSuper* this) ret 0, returns 1, 0 or -1 | Picks the Greek First Division champion and the Greek Cup winner, or the league runner-up when one club wins both. | high | opus |  |
| 0x5ec6b0 | 125 | `GreSuper::start_new_season` | thiscall(GreSuper* this) ret 0 | Clears the finished Greek Super Cup, archives its stats, moves the year on and sets up the clubs and rounds again. | high | opus |  |
