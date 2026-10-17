# wel_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x924420 | 130 (+2 unwind) | `WelCup::WelCup` | thiscall(WelCup* this, short season_year, CompRecord* comp) ret 8, returns this | Constructs the Welsh cup on Cup, loads saved data or collects entrants, and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x9245f0 | 11 | `WelCup::`scalar deleting destructor'` | thiscall(WelCup* this, unsigned flags) ret 4, returns this | Runs the Welsh cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x924610 | 62 (+1 unwind) | `WelCup::~WelCup` | thiscall(WelCup* this) ret 0 | Destroys the Welsh cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x9246e0 | 249 | `WelCup::create_round_table` | thiscall(WelCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the five-round table of the Welsh cup for stage -1 with draw dates, match dates and round rules, starting with 32 teams. | high | opus |  |
| 0x924ab0 | 126 | `WelCup::collect_entrants` | thiscall(WelCup* this) ret 0, returns 1 when 32 entries fill, 0 when short, -1 on allocation failure | Fills the 32-entry Welsh Cup entrant list with up to 14 Welsh lower division clubs, then clubs of the Welsh premier division. | high | sonnet |  |
| 0x924c50 | 132 | `WelCup::start_new_season` | thiscall(WelCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the entrants, rounds, fixture tree and ranking. | high | opus | 2026-10-16-research-name-check.md |
| 0x924e00 | 16 | `WelCup::set_up_rounds` | thiscall(WelCup* this) ret 0, returns 1 | Sets a prize fund of 50000 and builds the round table of the Welsh cup. | high | opus |  |
