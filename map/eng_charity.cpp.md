# eng_charity.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x56d380 | 132 (+2 unwind) | `EngCharity::EngCharity` | thiscall(EngCharity* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the Charity Shield cup, loads its saved state or picks its two teams, builds the one-round table and the fixture tree. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x56d550 | 11 | `EngCharity::`scalar deleting destructor'` | thiscall(EngCharity* this, unsigned flags) ret 4, returns this | Destroys the Charity Shield cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x56d570 | 62 (+1 unwind) | `EngCharity::~EngCharity` | thiscall(EngCharity* this) ret 0 | Restores the Charity Shield vtable, frees the team, round and tie arrays and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x56d640 | 98 | `EngCharity::create_round_table` | thiscall(EngCharity* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the single-round table of the Charity Shield, with one match, a draw date and a match date in August. | high | opus |  |
| 0x56d780 | 165 | `EngCharity::select_teams` | thiscall(EngCharity* this) ret 0, returns 1 on success, 0 when a club is missing, -1 on allocation failure | Picks the league champion and the FA Cup winner for the Charity Shield, and takes the league runner-up when one club won both. | high | opus |  |
| 0x56d9b0 | 132 | `EngCharity::start_new_season` | thiscall(EngCharity* this) ret 0 | Frees last season's Charity Shield data, archives the stats, moves the year on and picks the new teams and rounds. | high | opus |  |
