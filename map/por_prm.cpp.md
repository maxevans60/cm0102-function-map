# por_prm.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ce720 | 156 (+2 unwind) | `PorPrm::PorPrm` | thiscall(PorPrm* this, short year, CompRecord* comp) ret 8, returns this | Builds the Portuguese Premier Division on League, loads it from the temp file or sets rules, table, fixtures and statistics. | high | opus |  |
| 0x7ce930 | 11 | `PorPrm::`scalar deleting destructor'` | thiscall(PorPrm* this, unsigned flags) ret 4, returns this | Destroys the Portuguese Premier Division and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x7ce950 | 38 (+1 unwind) | `PorPrm::~PorPrm` | thiscall(PorPrm* this) ret 0 | Frees the table and the schedule and deletes the statistics object, then runs the League destructor. | high | opus |  |
| 0x7ce9e0 | 1544 | `PorPrm::create_schedule` | thiscall(PorPrm* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 34-round schedule template of the Premier Division from late August, with three match slots on most rounds. | high | opus |  |
| 0x7cf800 | 99 | `PorPrm::create_table` | thiscall(PorPrm* this) ret 0, returns 1 on success and 0 on failure | Allocates the 18-row table, fills it with the Premier Division clubs, sets the prize fund and pays each club 1000000. | high | opus |  |
| 0x7cf930 | 41 | `PorPrm::set_up_rules` | thiscall(PorPrm* this) ret 0, returns 1 | Sets the Premier Division rules with relegation to the Second Division 0x9cf610 and builds its schedule. | high | opus |  |
| 0x7cf9e0 | 159 | `PorPrm::start_new_season` | thiscall(PorPrm* this) ret 0 | Runs B team checks and promotion and relegation, rebuilds the table and fixtures, then starts the new season of the lower divisions. | high | opus |  |
| 0x7cfbf0 | 91 | `PorPrm::process_promotion_relegation_chain` | thiscall(PorPrm* this, int unused) ret 4, this unused | Records final positions and moves clubs between the Premier and Second Divisions, and between the Second Division and both Second Division B stages. | high | opus |  |
| 0x7cfd30 | 193 | `PorPrm::exchange_second_division_with_zones` | thiscall(PorPrm* this) ret 0 | When Second Division B is not played, relegates the marked Second Division clubs to the north zone and promotes as many shuffled zone clubs. | high | sonnet |  |
| 0x7cff70 | 214 | `por_prm_exchange_second_b_with_lower` | cdecl(void) ret 0 | Relegates marked clubs of Second Division B and its stages to the Third Division, then promotes as many shuffled lower Portuguese clubs into Second Division B. | high | sonnet |  |
| 0x7d0210 | 91 | `por_prm_assign_second_b_zones` | cdecl(void) ret 0 | Sorts up to 60 Second Division B clubs by stadium latitude and sets zones: 20 south, 20 central, the rest north. | high | sonnet |  |
| 0x7d0320 | 468 | `PorPrm::apply_b_team_promotion_limits` | thiscall(PorPrm* this) ret 0 | Relegates B teams whose senior club drops into their division, blocks B team promotion to the senior club's division and rebalances the other promotion marks. | high | sonnet |  |
