# bra_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x427430 | 134 (+2 unwind) | `BraCup::BraCup` | thiscall(BraCup* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the Brazilian Cup on Cup, then loads its saved state or selects the entrants, builds the team and round tables and ranks the teams. | high | opus |  |
| 0x427610 | 11 | `BraCup::`scalar deleting destructor'` | thiscall(BraCup* this, unsigned flags) ret 4, returns this | Destroys the Brazilian Cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x427630 | 62 (+1 unwind) | `BraCup::~BraCup` | thiscall(BraCup* this) ret 0, ECX is this | Frees the team table, round table and per-round arrays and the statistics of the Brazilian Cup, then runs the Cup destructor. | high | opus |  |
| 0x427700 | 324 | `BraCup::create_round_table` | thiscall(BraCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the seven-round table of the Brazilian Cup with draw dates, match dates and round rules. | high | opus |  |
| 0x427c20 | 65 | `BraCup::build_team_table` | thiscall(BraCup* this) ret 0, returns 1 or -1 on failure | Sets the team count to 71 and builds the six-byte team table from the entrant list, clearing the status bytes. | high | opus |  |
| 0x427d10 | 132 | `BraCup::start_new_season` | thiscall(BraCup* this) ret 0 | Frees last season's tables, archives the statistics, moves the year on and rebuilds the team table and rounds, then ranks the teams. | high | opus |  |
| 0x427ec0 | 18 | `BraCup::set_up_rounds` | thiscall(BraCup* this) ret 0, returns 1 | Sets the round rules and a prize fund of 500000 and builds the round table of the Brazilian Cup. | high | opus |  |
| 0x427f00 | 2293 | `BraCup::select_entrants` | thiscall(BraCup* this) ret 0 | Allocates the 71-slot entrant list and fills it with named Brazilian clubs, then with clubs of the state leagues sorted by strength. | high | opus |  |
