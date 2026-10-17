# ita_ser_c2c.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x65b4e0 | 161 (+2 unwind) | `ItaSerC2c::ItaSerC2c` | thiscall(ItaSerC2c* this, short year, void* comp_record) ret 8, returns this | Constructs the Serie C2 group C league and, without saved data, sets up its rules, table, fixed fixtures, schedule and stats. | high | opus |  |
| 0x65b710 | 11 | `ItaSerC2c::`scalar deleting destructor'` | thiscall(ItaSerC2c* this, unsigned flags) ret 4, returns this | Runs the Serie C2 group C destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x65b730 | 57 (+1 unwind) | `ItaSerC2c::~ItaSerC2c` | thiscall(ItaSerC2c* this) ret 0 | Destroys the Serie C2 group C league by freeing its table, schedule, play-off stages and stats, then runs the League destructor. | high | opus |  |
| 0x65b7f0 | 927 | `ItaSerC2c::create_schedule` | thiscall(ItaSerC2c* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns schedule pointer or null | Builds the 34-round league schedule for stage -1, the two-round promotion play-off for stage 0 and the two-leg relegation play-out for stage 1. | high | opus |  |
| 0x65c0e0 | 84 | `ItaSerC2c::init_team_list` | thiscall(ItaSerC2c* this) ret 0, returns bool | Sets the team count to 18, allocates the league table and fills one row for each club whose division is Serie C2 group C. | high | opus |  |
| 0x65c1e0 | 42 | `ItaSerC2c::set_up_rules` | thiscall(ItaSerC2c* this) ret 0, returns 1 | Sets the points, promotion, play-off and relegation counts of Serie C2 group C, links the sibling groups and builds the league schedule. | high | opus |  |
| 0x65c290 | 143 | `ItaSerC2c::start_new_season` | thiscall(ItaSerC2c* this) ret 0 | Clears the finished Serie C2 group C season, archives its stats, moves the year on and builds the rules, table and fixtures again. | high | opus |  |
| 0x65c450 | 40 | `ItaSerC2c::advance_stage` | thiscall(ItaSerC2c* this) ret 0 | Moves the stage counter on and builds the play-off stages at stage 0, or asserts when it passes the last stage. | high | opus |  |
| 0x65c4e0 | 223 (+2 unwind) | `ItaSerC2c::create_playoff_stages` | thiscall(ItaSerC2c* this) ret 0 | Builds the promotion play-off Cup_Stage for table places 2 to 5 and the relegation play-out Cup_Stage for places 14 to 17. | high | opus |  |
| 0x65c7d0 | 65 | `ItaSerC2c::set_club_progress` | thiscall(ItaSerC2c* this, Club* club, char stage, char current, char best, char worst) ret 0x14 | Maps the play-off stage codes of a club to league position codes and writes the three progress bytes of its Comp_Stats entry. | high | opus |  |
| 0x65c8e0 | 2861 (+1 unwind) | `ItaSerC2c::load_fixed_fixtures` | thiscall(ItaSerC2c* this) ret 0 | Allocates the fixed fixture table and enters the real 2001 to 2002 Serie C2 group C fixtures by club name and date. | high | opus | 2026-10-16-sweep-season-end.md |
