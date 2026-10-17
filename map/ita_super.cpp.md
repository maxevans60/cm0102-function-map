# ita_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x65f670 | 128 (+2 unwind) | `ItaSuper::ItaSuper` | thiscall(ItaSuper* this, short year, void* comp_record) ret 8, returns this | Constructs the Italian Super Cup and, without saved data, picks its two clubs and builds its round table, tie tree and stats. | high | opus |  |
| 0x65f830 | 11 | `ItaSuper::`scalar deleting destructor'` | thiscall(ItaSuper* this, unsigned flags) ret 4, returns this | Runs the Italian Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x65f850 | 62 (+1 unwind) | `ItaSuper::~ItaSuper` | thiscall(ItaSuper* this) ret 0 | Destroys the Italian Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x65f920 | 98 | `ItaSuper::create_round_table` | thiscall(ItaSuper* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* or null | Builds the one-round, one-leg table of the Italian Super Cup with its draw and match dates for two clubs. | high | opus |  |
| 0x65fa60 | 165 | `ItaSuper::init_team_list` | thiscall(ItaSuper* this) ret 0, returns 1, 0 or -1 | Sets two teams and fills the team list with the Serie A champions and Coppa Italia winners, or the cup runners-up when they match. | high | opus |  |
| 0x65fc90 | 125 | `ItaSuper::start_new_season` | thiscall(ItaSuper* this) ret 0 | Clears the finished Italian Super Cup, archives its stats, moves the year on and picks the clubs and rounds again. | high | opus |  |
