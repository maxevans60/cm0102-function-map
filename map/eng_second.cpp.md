# eng_second.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5754a0 | 159 (+2 unwind) | `EngSecond::EngSecond` | thiscall(EngSecond* this, short year, club_comp* comp) ret 8, returns this | Constructs the English Second Division on the League base, loads it from the temp file or sets up its rules, table, fixtures and stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x5756c0 | 11 | `EngSecond::`scalar deleting destructor'` | thiscall(EngSecond* this, unsigned flags) ret 4, returns this | Runs the Second Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5756e0 | 60 (+1 unwind) | `EngSecond::~EngSecond` | thiscall(EngSecond* this) ret 0 | Destroys the Second Division by freeing its table, schedule, stage objects and stats, then runs the League destructor. | high | opus |  |
| 0x5757a0 | 1607 | `EngSecond::create_schedule` | thiscall(EngSecond* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 46-matchday league schedule for stage -1 or the two-round play-off table for stage 0, with dates in the season year. | high | opus |  |
| 0x576630 | 103 | `EngSecond::create_table` | thiscall(EngSecond* this) ret 0, returns 1 on success | Allocates the 24-row league table, fills it with the Second Division clubs, sets the prize fund and pays the clubs. | high | opus |  |
| 0x576780 | 37 | `EngSecond::set_up_rules` | thiscall(EngSecond* this) ret 0, returns 1 | Sets the Second Division rules with two promoted clubs, four play-off places and four relegated clubs, then builds the league schedule. | high | opus |  |
| 0x576820 | 143 | `EngSecond::start_new_season` | thiscall(EngSecond* this) ret 0 | Clears the old season, archives the stats, moves the year on and rebuilds the rules, table, fixtures and predicted positions. | high | opus |  |
| 0x5769e0 | 40 | `EngSecond::advance_stage` | thiscall(EngSecond* this) ret 0 | Moves the division to its next stage and builds the play-off stage when stage 0 starts, or reports an error after the last stage. | high | opus |  |
| 0x576a70 | 138 (+1 unwind) | `EngSecond::create_play_off_stage` | thiscall(EngSecond* this) ret 0 | Takes the clubs in third to sixth place, builds the four-club play-off Cup_Stage and sets up its first round. | high | opus |  |
| 0x576c50 | 141 | `EngSecond::update_staff_records_for_status` | thiscall(EngSecond* this, Club* club, char status, char stage, bool* removed) ret 0x18 | Adds league champion, promotion, play-off or relegation records to the staff history of a club, and marks play-off losers in the table. | high | opus |  |
