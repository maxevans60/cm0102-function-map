# nor_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x78f020 | 132 (+2 unwind) | `NorCup::NorCup` | thiscall(NorCup* this, short comp_id, int owner) ret 8, returns this | Constructs the Norwegian cup on Cup, then loads saved data or collects entrants, builds the round table, fixture tree, Comp_Stats and ranking. | high | opus |  |
| 0x78f1f0 | 11 | `NorCup::`scalar deleting destructor'` | thiscall(NorCup* this, unsigned flags) ret 4, returns this | Runs the Norwegian cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x78f210 | 62 (+1 unwind) | `NorCup::~NorCup` | thiscall(NorCup* this) ret 0 | Destroys the Norwegian cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x78f2e0 | 375 (+1 unwind) | `NorCup::create_round_table` | thiscall(NorCup* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns round table | Allocates and fills the seven-round table of the Norwegian cup from April, with draw dates, match dates, round rules and a weekday-checked final date. | high | opus |  |
| 0x78f890 | 227 | `NorCup::collect_entrants` | thiscall(NorCup* this) ret 0, returns 1 when 128 entrants are found, 0 when short, -1 on allocation failure | Fills the 128-entry six-byte entrant list with Norwegian league clubs, flagging the top division, then another division and then clubs without a division. | high | opus |  |
| 0x78fb90 | 132 | `NorCup::start_new_season` | thiscall(NorCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus |  |
