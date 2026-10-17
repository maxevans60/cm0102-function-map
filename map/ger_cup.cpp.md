# ger_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5d8c20 | 132 (+2 unwind) | `GerCup::GerCup` | thiscall(GerCup* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the German cup, loads it from the temp file or collects entrants, builds rounds, fixture tree and Comp_Stats, reporting errors by assert box. | high | opus |  |
| 0x5d8df0 | 11 | `GerCup::`scalar deleting destructor'` | thiscall(GerCup* this, unsigned flags), returns this, ret 4 | Destroys the German cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x5d8e10 | 62 (+1 unwind) | `GerCup::~GerCup` | thiscall(GerCup* this), ret 0 | Restores the vtable, frees the entrant list, round table and stage objects and the Comp_Stats member, then runs the Cup base destructor. | high | opus |  |
| 0x5d8ee0 | 299 | `GerCup::create_round_table` | thiscall(GerCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the six-round table of the German cup with draw dates, match dates and round rules, starting with 64 teams. | high | opus |  |
| 0x5d9370 | 310 | `GerCup::collect_entrants` | thiscall(GerCup* this) ret 0, returns 1 when 64 entries fill, 0 when short, -1 on allocation failure | Fills the 64-entry six-byte entrant list with shuffled lower German clubs, then the Second and First Bundesliga clubs. | high | opus |  |
| 0x5d9780 | 132 | `GerCup::start_new_season` | thiscall(GerCup* this) ret 0 | Frees the entrant list, round table and rounds, archives the stats, moves the year on and collects entrants and rounds for the new season. | high | opus |  |
| 0x5d9930 | 51 | `GerCup::club_in_higher_division` | thiscall(GerCup* this unused, Club* a, Club* b) ret 8, returns a club or 0 | Returns the club outside the two Bundesliga divisions when its opponent plays in one of them, or none when both or neither do. | high | opus |  |
