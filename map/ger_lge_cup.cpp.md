# ger_lge_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5dc0e0 | 132 (+2 unwind) | `GerLgeCup::GerLgeCup` | thiscall(GerLgeCup* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the German League Cup on Cup, then loads saved data or collects its six entrants, rounds, fixture tree, Comp_Stats and ranking. | high | opus |  |
| 0x5dc2b0 | 11 | `GerLgeCup::`scalar deleting destructor'` | thiscall(GerLgeCup* this, unsigned flags), returns this, ret 4 | Runs the GerLgeCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5dc2d0 | 62 (+1 unwind) | `GerLgeCup::~GerLgeCup` | thiscall(GerLgeCup* this), ret 0 | Destroys the German League Cup, freeing its entrant list, round table, per-round tie arrays and Comp_Stats before the Cup destructor runs. | high | opus |  |
| 0x5dc3a0 | 286 | `GerLgeCup::create_round_table` | thiscall(GerLgeCup* this, char stage, short* round_count, short* extra, int* out), returns round table pointer, ret 0x10 | Builds the three-round table of the German League Cup for stage -1 with draw dates, match dates and progression rules. | high | opus |  |
| 0x5dc700 | 229 | `GerLgeCup::collect_entrants` | thiscall(GerLgeCup* this), ret 0, returns 1 on success, 0 or -1 on failure | Fills the six-entry list with the top six of last season's First Division, seeding the German Cup winner into the later round. | high | opus |  |
| 0x5dc9e0 | 132 | `GerLgeCup::start_new_season` | thiscall(GerLgeCup* this), ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
| 0x5dcb90 | 18 | `GerLgeCup::set_up_rounds` | thiscall(GerLgeCup* this), returns 1, ret 0 | Sets six entrants, three rounds and a 500000 prize fund, then builds the round table for stage -1. | high | opus |  |
