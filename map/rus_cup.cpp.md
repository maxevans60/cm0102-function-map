# rus_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7e9210 | 141 (+2 unwind) | `RusCup::RusCup` | thiscall(RusCup* this, short year, void* comp_record) ret 8, returns this | Constructs the Russian Cup, loads it or selects its 48 entrants, builds the round table and fixture tree, and ranks the teams. | high | opus |  |
| 0x7e9400 | 11 | `RusCup::`scalar deleting destructor'` | thiscall(RusCup* this, unsigned flags) ret 4, returns this | Runs the RusCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7e9420 | 84 (+1 unwind) | `RusCup::~RusCup` | thiscall(RusCup* this) ret 0 | Destroys the Russian Cup, freeing its team list, round arrays, Comp_Stats and stage objects, then runs the Cup destructor. | high | opus |  |
| 0x7e9530 | 289 | `RusCup::create_round_table` | thiscall(RusCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table | Builds the six-round table of the Russian Cup with dates, team counts and replay rules for each round. | high | opus |  |
| 0x7e99a0 | 258 | `RusCup::select_entrants` | thiscall(RusCup* this) ret 0, returns 1 when 48 teams are placed, -1 on failure | Fills the 48-team entry list with top-flight clubs, second-division clubs and 14 shuffled lower-zone clubs, marking the holder. | medium | opus |  |
| 0x7e9d10 | 132 | `RusCup::start_new_season` | thiscall(RusCup* this) ret 0 | Frees last season's team list and round data, increments the year, selects new entrants, sets up the rounds and refreshes rankings. | high | opus |  |
| 0x7e9ec0 | 41 | `RusCup::update_for_date` | thiscall(RusCup* this, Date* date, int phase) ret 8 | Starts a new cup season on 1 May when the cup is complete, then runs the base Cup date update. | high | opus |  |
