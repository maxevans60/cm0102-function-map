# por_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7cd980 | 130 (+2 unwind) | `PorCup::PorCup` | thiscall(PorCup* this, short year, CompRecord* comp) ret 8, returns this | Builds the Portuguese Cup on Cup, loads it from disk or collects its entrants, builds the round table, fixture tree and statistics. | high | opus |  |
| 0x7cdb50 | 11 | `PorCup::`scalar deleting destructor'` | thiscall(PorCup* this, unsigned flags) ret 4, returns this | Destroys the Portuguese Cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x7cdb70 | 62 (+1 unwind) | `PorCup::~PorCup` | thiscall(PorCup* this) ret 0 | Frees the entrant list, round table and tie arrays and the statistics object, then runs the Cup destructor. | high | opus |  |
| 0x7cdc40 | 362 | `PorCup::create_round_table` | thiscall(PorCup* this, char stage, short* round_count, short* extra, int* is_league) ret 0x10, returns round table | Allocates the eight-round Portuguese Cup table and sets the draw date, match dates, ties and rules of each round. | high | opus |  |
| 0x7ce220 | 241 | `PorCup::collect_entrants` | thiscall(PorCup* this) ret 0, returns 1 when full, 0 when short, -1 on allocation failure | Fills the 164-place entrant list with Portuguese clubs from the lowest divisions upwards, skipping B teams, then swaps the last entrant at random. | high | opus |  |
| 0x7ce540 | 132 | `PorCup::start_new_season` | thiscall(PorCup* this) ret 0 | Frees last season's tables, archives the statistics, adds one to the year and rebuilds the entrants, round table and stages. | high | opus |  |
| 0x7ce6f0 | 16 | `PorCup::set_up_rounds` | thiscall(PorCup* this) ret 0, returns 1 | Sets a prize fund of 800000 and builds the round table, a body that four other cups share by the same pointer. | high | opus |  |
