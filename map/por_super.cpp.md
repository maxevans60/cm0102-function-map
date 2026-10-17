# por_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7d2e40 | 126 (+2 unwind) | `PorSuper::PorSuper` | thiscall(PorSuper* this, short year, void* comp_record) ret 8, returns this | Constructs the Portuguese Super Cup, loads it or selects the two teams, builds the round table and fixture tree, and creates Comp_Stats. | high | opus |  |
| 0x7d3000 | 11 | `PorSuper::`scalar deleting destructor'` | thiscall(PorSuper* this, unsigned flags) ret 4, returns this | Runs the PorSuper destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7d3020 | 62 (+1 unwind) | `PorSuper::~PorSuper` | thiscall(PorSuper* this) ret 0 | Destroys the Super Cup, freeing its team list, round table, round arrays and Comp_Stats, then runs the Cup destructor. | high | opus |  |
| 0x7d30f0 | 111 | `PorSuper::create_round_table` | thiscall(PorSuper* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table | Builds the one-round table of the Super Cup, a two-legged final, with a different second-leg setting in the 2000 season. | high | opus |  |
| 0x7d3260 | 165 | `PorSuper::select_teams` | thiscall(PorSuper* this) ret 0, returns 1, 0 or -1 | Picks the league champion and the cup winner as the two Super Cup teams, taking the cup runner-up when one club won both. | high | opus |  |
| 0x7d3490 | 125 | `PorSuper::start_new_season` | thiscall(PorSuper* this) ret 0 | Frees last season's team list and round data, increments the year, selects the new teams and sets up the rounds. | high | opus |  |
