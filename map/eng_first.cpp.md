# eng_first.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x571680 | 159 (+2 unwind) | `EngFirst::EngFirst` | thiscall(EngFirst* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the English First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x5718a0 | 11 | `EngFirst::`scalar deleting destructor'` | thiscall(EngFirst* this, unsigned flags), returns this, ret 4 | Runs the EngFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5718c0 | 60 (+1 unwind) | `EngFirst::~EngFirst` | thiscall(EngFirst* this), ret 0 | Destroys the English First Division, freeing its table, schedule, play-off stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x571980 | 2070 | `EngFirst::create_schedule` | thiscall(EngFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 46-round league schedule for stage -1 and the two-round play-off table for stage 0, returning null otherwise. | high | opus |  |
| 0x572bf0 | 129 | `EngFirst::create_table` | thiscall(EngFirst* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 24-row table, fills it with First Division clubs, sets the prize fund and pays TV money by year and previous division. | high | opus |  |
| 0x572d90 | 36 | `EngFirst::set_up_rules` | thiscall(EngFirst* this), returns 1, ret 0 | Sets the First Division rule bytes, with the Premier Division above and the Second Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x572e30 | 143 | `EngFirst::start_new_season` | thiscall(EngFirst* this), ret 0 | Frees the table, schedule and play-off stages, archives the season, moves the year on and rebuilds rules, table and fixtures. | high | opus |  |
| 0x572ff0 | 40 | `EngFirst::advance_stage` | thiscall(EngFirst* this), ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the promotion play-off stage when the counter reaches 0. | high | opus |  |
| 0x573080 | 136 (+1 unwind) | `EngFirst::create_playoff_stage` | thiscall(EngFirst* this), ret 0 | Builds the First Division play-off Cup_Stage from the clubs in third to sixth place and sets up its first round. | high | opus |  |
| 0x573260 | 102 | `EngFirst::set_club_progress` | thiscall(EngFirst* this, Club* club, char stage, char current, char best, char worst), ret 0x14 | Stores three progress codes of a club in Comp_Stats, folding league places 3 to 6 into 3 and play-off rounds into codes 3 to 5. | high | opus |  |
