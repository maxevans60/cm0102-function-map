# fra_lge_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5bc980 | 133 (+2 unwind) | `FraLgeCup::FraLgeCup` | thiscall(FraLgeCup* this, short year, void* comp_record), ret 8 | Constructs the French League Cup on Cup and, when no saved data loads, collects its entrants and builds its rounds, tie tree, stats and ranking. | high | opus |  |
| 0x5bcb50 | 11 | `FraLgeCup::`scalar deleting destructor'` | thiscall(FraLgeCup* this, unsigned flags), ret 4, returns this | Runs the French League Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bcb70 | 62 (+1 unwind) | `FraLgeCup::~FraLgeCup` | thiscall(FraLgeCup* this), ret 0 | Destroys the French League Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x5bcc40 | 324 | `FraLgeCup::create_round_table` | thiscall(FraLgeCup* this, char stage, short* round_count, short* extra, int* out), ret 0x10, returns Round* or null | Allocates and fills the seven-round table of the French League Cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x5bd160 | 215 | `FraLgeCup::collect_entrants` | thiscall(FraLgeCup* this), ret 0, returns 1 when 54 entries fill, 0 when short, -1 on allocation failure | Fills the 54-entry six-byte entrant list with third-division clubs in two passes, then Second Division clubs, then First Division clubs. | high | opus |  |
| 0x5bd420 | 132 | `FraLgeCup::start_new_season` | thiscall(FraLgeCup* this), ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds and fixture tree for the new season. | high | opus |  |
| 0x5bd5d0 | 16 | `FraLgeCup::set_up_rounds` | thiscall(FraLgeCup* this), ret 0, returns 1 | Sets the French League Cup prize fund to 500000 and stores the round table built for the whole cup at this+0xa3. | high | opus |  |
