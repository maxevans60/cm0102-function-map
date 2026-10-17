# tur_first.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8fcf60 | 156 (+2 unwind) | `TurFirst::TurFirst` | thiscall(TurFirst* this, short season, int nation), ret 8 | Constructs the Turkish first division, loads it from the temp file or sets its rules, table, fixtures and stats. | high | opus |  |
| 0x8fd170 | 11 | `TurFirst::`scalar deleting destructor'` | thiscall(TurFirst* this, unsigned flags), ret 4 | Destroys the Turkish first division and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x8fd190 | 38 (+1 unwind) | `TurFirst::~TurFirst` | thiscall(TurFirst* this), ret 0 | Restores the Turkish first division vtable, frees its table and schedule, deletes the stats and runs the League destructor. | high | opus |  |
| 0x8fd220 | 1264 | `TurFirst::create_schedule` | thiscall(TurFirst* this, char stage, short* round_count, short* extra, int* out), ret 0x10 | Builds the 34-round Turkish first division schedule with a date and match slots for each round. | high | opus |  |
| 0x8fddc0 | 146 | `TurFirst::create_table` | thiscall(TurFirst* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 18-row table, fills it with the Turkish premier clubs and pays each club 1000000, merging the third tier groups in 2001. | high | opus | 2026-10-16-season-change-points.md |
| 0x8fdf90 | 41 | `TurFirst::set_up_rules` | thiscall(TurFirst* this), returns 1, ret 0 | Sets the Turkish first division rules, with no higher division and one lower competition, and builds its schedule. | high | opus |  |
| 0x8fe040 | 159 | `TurFirst::start_new_season` | thiscall(TurFirst* this), ret 0 | Runs Turkish promotion and relegation and the third tier reshuffle, then rebuilds the table, fixtures and rules for the new season. | high | opus |  |
| 0x8fe250 | 102 | `TurFirst::process_promotion_relegation_chain` | thiscall(TurFirst* this, int pairwise), ret 4 | Records final positions in the three Turkish divisions and moves clubs between the premier, second and third tier groups. | high | opus |  |
| 0x8fe3a0 | 158 | `tur_first_promote_lower_clubs_to_third_tier` | cdecl(void), ret 0 | Moves the top ten clubs of the lowest Turkish division into the third tier and drops each relegated third tier club down. | medium | opus |  |
| 0x8fe580 | 115 | `tur_first_assign_third_tier_groups` | cdecl(void), ret 0 | Sorts up to 50 third tier Turkish clubs by longitude and puts them ten at a time into the five regional groups. | high | opus |  |
