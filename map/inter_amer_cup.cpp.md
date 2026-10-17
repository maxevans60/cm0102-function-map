# inter_amer_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x632080 | 133 (+2 unwind) | `InterAmerCup::InterAmerCup` | thiscall(InterAmerCup* this, short comp_id, int owner), returns this, ret 8 | Runs the Cup constructor, installs vtable 0x96bad8, loads the saved cup or selects the two clubs and builds the rounds, tree and statistics. | high | opus | club-world.md |
| 0x632250 | 11 | `InterAmerCup::`scalar deleting destructor'` | thiscall(InterAmerCup* this, unsigned flags), ret 4 | Runs the InterAmerCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x632270 | 62 (+1 unwind) | `InterAmerCup::~InterAmerCup` | thiscall(InterAmerCup* this), ret 0 | Restores the vtable, frees the team list, round table and stage arrays and the statistics, then runs the Cup destructor. | high | opus |  |
| 0x632340 | 98 | `InterAmerCup::create_round_table` | thiscall(InterAmerCup* this, char stage, short* round_count, short* extra, int* out), returns round table, ret 0x10 | Allocates a one-round table for the two-legged Inter-American Cup final with its draw and match dates. | high | opus | 2026-10-16-sweep-europe.md |
| 0x632480 | 333 | `InterAmerCup::select_teams` | thiscall(InterAmerCup* this), returns 1, 0 or -1, ret 0 | Picks the two finalists, one strong club from each of two American continents, or the latest winners of two feeder cups. | medium | opus |  |
| 0x632910 | 132 | `InterAmerCup::start_new_season` | thiscall(InterAmerCup* this), ret 0 | Frees the season data, archives the statistics, advances the year, then selects the clubs and rebuilds rounds and stages for the next edition. | high | opus |  |
