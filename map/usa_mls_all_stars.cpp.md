# usa_mls_all_stars.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x90a150 | 126 (+2 unwind) | `UsaMlsAllStars::UsaMlsAllStars` | thiscall(UsaMlsAllStars* this, short year, Comp* comp) ret 8, returns this | Builds the MLS All-Star game cup on Cup, sets up its two teams, round table and fixture tree, and creates the Comp_Stats object. | high | opus |  |
| 0x90a310 | 11 | `UsaMlsAllStars::`scalar deleting destructor'` | thiscall(UsaMlsAllStars* this, unsigned flags) ret 4, returns this | Runs the All-Stars destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x90a330 | 62 (+1 unwind) | `UsaMlsAllStars::~UsaMlsAllStars` | thiscall(UsaMlsAllStars* this) ret 0 | Restores the All-Stars vtable, frees the team list, round table and tie arrays and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x90a400 | 98 | `UsaMlsAllStars::create_round_table` | thiscall(UsaMlsAllStars* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table | Builds the one-round table of the All-Star game with its draw date and match date. | high | opus |  |
| 0x90a540 | 160 | `UsaMlsAllStars::set_up_teams` | thiscall(UsaMlsAllStars* this) ret 0, returns 1 or -1 | Sets the two All-Star clubs as the teams, swaps home side by year, lends them a random host club's stadium and sets their nation. | high | sonnet |  |
| 0x90a760 | 125 | `UsaMlsAllStars::start_new_season` | thiscall(UsaMlsAllStars* this) ret 0 | Frees last year's All-Star data, archives the stats, moves the year on and rebuilds the teams, rounds and fixture tree. | high | opus | 2026-10-16-research-name-check.md |
| 0x90a900 | 41 (+1 unwind) | `UsaMlsAllStars::update_for_date` | thiscall(UsaMlsAllStars* this, Date* today, int phase) ret 8 | Selects both All-Star squads on the fixed squad date, day 26 of month index 6, then runs the base cup daily update. | high | opus |  |
| 0x90a980 | 366 (+2 unwind) | `UsaMlsAllStars::select_squads` | thiscall(UsaMlsAllStars* this) ret 0 | Collects fit MLS players by conference, sorts them and fills the squads of the two All-Star clubs, one for each conference. | high | opus |  |
