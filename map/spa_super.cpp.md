# spa_super.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8586b0 | 128 (+2 unwind) | `SpaSuper::SpaSuper` | thiscall(SpaSuper* this, short year, void* comp_record), ret 8, returns this | Constructs the Spanish Super Cup on Cup and, without saved data, picks its two clubs and builds its round table, tie tree and stats. | high | opus |  |
| 0x858870 | 11 | `SpaSuper::`scalar deleting destructor'` | thiscall(SpaSuper* this, unsigned flags), ret 4, returns this | Runs the Spanish Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x858890 | 62 (+1 unwind) | `SpaSuper::~SpaSuper` | thiscall(SpaSuper* this), ret 0 | Destroys the Spanish Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x858960 | 98 | `SpaSuper::create_round_table` | thiscall(SpaSuper* this, char stage, short* round_count, short* extra, int* out), ret 0x10, returns Round* or null | Builds the one-round, two-leg table of the Spanish Super Cup with its draw and match dates for two clubs. | high | opus |  |
| 0x858aa0 | 165 | `SpaSuper::select_teams` | thiscall(SpaSuper* this), ret 0, returns 1, 0 or -1 | Picks the Spanish cup winner and the Spanish First Division champion, or the cup runner-up when one club won both. | high | opus |  |
| 0x858cd0 | 125 | `SpaSuper::start_new_season` | thiscall(SpaSuper* this), ret 0 | Clears the finished Spanish Super Cup, archives its stats, moves the year on and picks the clubs and rounds again. | high | opus |  |
| 0x858e70 | 15 | `SpaSuper::set_up_rounds` | thiscall(SpaSuper* this), ret 0, returns 1 | Builds the round table from create_round_table with stage -1 and stores it at 0xa3, as the shared set-up of many simple cups. | high | opus | 2026-10-16-sweep-europe.md |
