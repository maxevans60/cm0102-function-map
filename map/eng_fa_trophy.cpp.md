# eng_fa_trophy.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x570c00 | 133 (+2 unwind) | `EngFaTrophy::EngFaTrophy` | thiscall(EngFaTrophy* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the FA Trophy on Cup, then loads saved data or selects the 32 clubs, builds the round table and fixture tree and creates Comp_Stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x570dd0 | 11 | `EngFaTrophy::`scalar deleting destructor'` | thiscall(EngFaTrophy* this, unsigned flags), returns this, ret 4 | Runs the FA Trophy destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x570df0 | 62 (+1 unwind) | `EngFaTrophy::~EngFaTrophy` | thiscall(EngFaTrophy* this), ret 0 | Destroys the FA Trophy, freeing its team list, round table, per-round tie arrays and Comp_Stats before the Cup destructor runs. | high | opus |  |
| 0x570ec0 | 255 | `EngFaTrophy::create_round_table` | thiscall(EngFaTrophy* this, char stage, short* round_count, short* extra, int* out_flag), returns round table pointer, ret 0x10 | Builds the five-round table of the FA Trophy with draw and match dates for stage -1 and returns null for other stages. | high | opus |  |
| 0x5712b0 | 143 | `EngFaTrophy::select_teams` | thiscall(EngFaTrophy* this), returns 1 when 32 clubs are found, 0 when short, -1 on allocation failure, ret 0 | Fills the 32-entry team list with the ten strongest English clubs outside the excluded divisions plus Conference clubs. | medium | opus |  |
| 0x5714a0 | 132 | `EngFaTrophy::start_new_season` | thiscall(EngFaTrophy* this), ret 0 | Frees the cup's working data, archives the season stats, moves the year on, then selects new teams and rebuilds the rounds and fixture tree. | high | opus |  |
| 0x571650 | 16 | `EngFaTrophy::set_up_rounds` | thiscall(EngFaTrophy* this), returns 1, ret 0 | Sets the cup prize fund to 300000 and stores the whole-cup round table at this+0xa3, for the FA Trophy and Charity Shield. | high | opus |  |
