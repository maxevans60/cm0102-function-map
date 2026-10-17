# pol_lge_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ca4e0 | 132 (+2 unwind) | `PolLgeCup::PolLgeCup` | thiscall(PolLgeCup* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Polish League Cup on Cup and, when no saved data loads, collects its entrants and builds its rounds, tie tree, stats and ranking. | high | opus |  |
| 0x7ca6b0 | 11 | `PolLgeCup::`scalar deleting destructor'` | thiscall(PolLgeCup* this, unsigned flags) ret 4, returns this | Runs the Polish League Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ca6d0 | 62 (+1 unwind) | `PolLgeCup::~PolLgeCup` | thiscall(PolLgeCup* this) ret 0 | Destroys the Polish League Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x7ca7a0 | 425 | `PolLgeCup::create_round_table` | thiscall(PolLgeCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* or null | Builds the six-round table of the Polish League Cup, with an extra opening round in 2001, setting draw dates, match dates and prize money. | high | opus |  |
| 0x7cad30 | 211 | `PolLgeCup::collect_entrants` | thiscall(PolLgeCup* this) ret 0, returns 1 when full, 0 when short, -1 on allocation failure | Fills the six-byte entrant list with 34 clubs, or 36 in 2001, from the Polish Second and First Divisions in four passes. | high | opus |  |
| 0x7cafe0 | 132 | `PolLgeCup::start_new_season` | thiscall(PolLgeCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds and fixture tree for the new season. | high | opus |  |
| 0x7cb190 | 18 | `PolLgeCup::set_up_rounds` | thiscall(PolLgeCup* this) ret 0, returns 1 | Sets the Polish League Cup prize fund to 400000 and stores the round table built for the whole cup at this+0xa3. | high | opus |  |
