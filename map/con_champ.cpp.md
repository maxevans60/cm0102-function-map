# con_champ.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4c0c40 | 131 (+2 unwind) | `ConChamp::ConChamp` | thiscall(ConChamp* this, short season_year, void* comp_record) ret 8 | Runs the Cup constructor, installs vtable 0x968aa0, loads the saved cup or builds an eight-club team table, round table, fixture tree and Comp_Stats. | high | opus | club-world.md |
| 0x4c0e10 | 11 | `ConChamp::`scalar deleting destructor'` | thiscall(ConChamp* this, unsigned flags) ret 4 | Runs the destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x4c0e30 | 62 (+1 unwind) | `ConChamp::~ConChamp` | thiscall(ConChamp* this) ret 0 | Restores the vtable, frees the team table, round table and per-round arrays, deletes the Comp_Stats object and runs the Cup destructor. | high | opus |  |
| 0x4c0f00 | 189 | `ConChamp::create_round_table` | thiscall(ConChamp* this, char stage, short* round_count, short* name_id, int* is_league) ret 0x10 | Allocates and fills the three-round knockout table of the cup with draw dates, match dates and progression rules for each round. | high | opus | 2026-10-16-sweep-europe.md |
| 0x4c11a0 | 191 | `ConChamp::select_qualified_clubs` | thiscall(ConChamp* this) ret 0, returns 1 | Fills the eight qualifier slots with two Mexican clubs, three and one from two regional groups, and the MLS and US Open Cup winners. | high | opus | 2026-10-16-sweep-europe.md |
| 0x4c1440 | 130 | `ConChamp::start_new_season` | thiscall(ConChamp* this) ret 0 | Frees the season data, archives the statistics, advances the season year, then rebuilds the team table, rounds and fixture tree for the next edition. | high | opus | 2026-10-16-research-name-check.md |
| 0x4c15f0 | 16 | `ConChamp::set_up_rounds` | thiscall(ConChamp* this) ret 0, returns 1 | Sets the prize fund to 2,000,000 and builds the round table through the create_round_table slot. | high | opus |  |
| 0x4c1620 | 56 | `ConChamp::update_for_date` | thiscall(ConChamp* this, Date* today, int full_update) ret 8 | Selects the qualified clubs and ranks them when the team table is still empty, then runs the base Cup daily update. | high | opus |  |
