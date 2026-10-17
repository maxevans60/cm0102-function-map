# eng_prm.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x573380 | 159 (+2 unwind) | `EngPrm::EngPrm` | thiscall(EngPrm* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the English Premier Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x5735b0 | 11 | `EngPrm::`scalar deleting destructor'` | thiscall(EngPrm* this, unsigned flags), returns this, ret 4 | Runs the EngPrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5735d0 | 38 (+1 unwind) | `EngPrm::~EngPrm` | thiscall(EngPrm* this), ret 0 | Destroys the English Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x573660 | 2123 | `EngPrm::create_schedule` | thiscall(EngPrm* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 38-round schedule template of the Premier Division for stage -1 and returns null otherwise. | high | opus |  |
| 0x574a20 | 103 | `EngPrm::create_table` | thiscall(EngPrm* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 20-row table, fills it with Premier Division clubs, sets the prize fund and pays each club 5000000, or 12000000 from 2000. | high | opus |  |
| 0x574b70 | 36 | `EngPrm::set_up_rules` | thiscall(EngPrm* this), returns 1, ret 0 | Sets the Premier Division rule bytes, with no upper league and the First Division below, and builds the schedule for stage -1. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x574c10 | 178 | `EngPrm::start_new_season` | thiscall(EngPrm* this), ret 0 | Runs promotion and relegation for the English pyramid, exchanges Conference clubs, rebuilds table and fixtures and restarts the lower leagues. | high | opus | 2026-10-16-sweep-season-end.md |
| 0x574e60 | 189 | `EngPrm::exchange_conference_clubs_unplayed` | thiscall(EngPrm* this) ret 0 | When the Conference is not played, promotes its strongest club to the Third Division if its ground passes, and moves relegated Third Division clubs down. | high | sonnet | 2026-10-16-sweep-season-end.md |
| 0x5750a0 | 196 | `EngPrm::exchange_conference_feeder_clubs` | thiscall(EngPrm* this) ret 0 | Promotes the best English club from each of three feeder divisions below the Conference, then moves the relegated Conference clubs into those divisions. | high | sonnet | 2026-10-16-sweep-season-end.md |
| 0x5752e0 | 5 | `EngPrm::process_promotion_relegation_chain` | thiscall(EngPrm* this, int pairwise), ret 4 | Entry of the slot that loads the Conference and Third Division pointers, then falls through into the chain body at 0x5752f0. | high | opus | 2026-10-16-sweep-season-end.md |
| 0x5752f0 | 137 | `EngPrm::process_promotion_relegation_chain_body` | thiscall(EngPrm* this, int pairwise), EAX and EBP preloaded by 0x5752e0, ret 4 | Records final positions and swaps clubs between the four Football League divisions, then promotes the Conference champion if its ground passes the check. | high | opus |  |
