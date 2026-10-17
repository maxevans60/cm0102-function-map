# nir_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x78a5b0 | 133 (+2 unwind) | `NirCup::NirCup` | thiscall(NirCup* this, short year, int nation), ret 8 | Constructs the Northern Irish Cup and, when no saved data loads, collects entrants and builds its rounds, fixture tree and Comp_Stats object. | high | opus |  |
| 0x78a780 | 11 | `NirCup::`scalar deleting destructor'` | thiscall(NirCup* this, unsigned flags), ret 4 | Destroys the Northern Irish Cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x78a7a0 | 62 (+1 unwind) | `NirCup::~NirCup` | thiscall(NirCup* this), ret 0 | Restores the cup vtable, frees the team, round and tie arrays and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x78a870 | 277 | `NirCup::create_round_table` | thiscall(NirCup* this, char stage, short* round_count, short* extra, int* out), ret 0x10 | Builds the five-round knockout table of the Irish Cup, from 32 clubs down to the final, with draw dates, match dates and prize money. | high | opus |  |
| 0x78ac90 | 119 | `NirCup::collect_entrants` | thiscall(NirCup* this) ret 0, returns 1, or -1 on allocation failure | Fills the 32-entry entrant list with twelve shuffled Northern Irish lower division clubs, then all Premier and First Division clubs. | high | opus | 2026-10-16-research-name-check.md, wal-nir-irl.md |
| 0x78ae30 | 132 | `NirCup::start_new_season` | thiscall(NirCup* this), ret 0 | Frees last season's cup data, archives the stats, moves the year on and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus |  |
| 0x78afe0 | 16 | `NirCup::set_up_rounds` | thiscall(NirCup* this) ret 0, returns 1 | Sets a prize fund of zero and builds the round table of the cup through slot 15. | high | opus |  |
