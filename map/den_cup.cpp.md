# den_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5509b0 | 132 (+2 unwind) | `DenCup::DenCup` | thiscall(DenCup* this, short comp_id, CompRecord* comp) ret 8, returns this | Constructs the Danish cup on Cup, then loads saved data or collects entrants, builds the round table, fixture tree and stats and ranks the teams. | high | opus |  |
| 0x550b80 | 11 | `DenCup::`scalar deleting destructor'` | thiscall(DenCup* this, unsigned flags) ret 4, returns this | Runs the Danish cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x550ba0 | 62 (+1 unwind) | `DenCup::~DenCup` | thiscall(DenCup* this) ret 0 | Destroys the Danish cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x550c70 | 362 | `DenCup::create_round_table` | thiscall(DenCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the eight-round table of the Danish cup with draw dates, match dates and round rules for stage -1, and returns null otherwise. | high | opus |  |
| 0x551240 | 211 | `DenCup::collect_entrants` | thiscall(DenCup* this) ret 0, returns 1 when 92 entries fill, 0 when short, -1 on allocation failure | Fills the 92-entry six-byte entrant list with Danish lower division, Second Division, First Division and Premier Division clubs in that order. | high | opus |  |
| 0x551500 | 132 | `DenCup::start_new_season` | thiscall(DenCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus |  |
| 0x5516b0 | 18 | `DenCup::set_up_rounds` | thiscall(DenCup* this) ret 0, returns 1 | Sets a prize fund of 800000 and the round rules and builds the round table of the Danish cup. | high | opus |  |
