# ita_ser_c2b.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x657350 | 161 (+2 unwind) | `ItaSerC2b::ItaSerC2b` | thiscall(ItaSerC2b* this, short year, void* comp_record) ret 8, returns this | Constructs the Serie C2 group B league and, without saved data, sets up its rules, table, fixed fixtures, schedule and stats. | high | opus |  |
| 0x65746c | 28 | `ItaSerC2b::ItaSerC2b_fragment_65746c` | not a function: mid-body chunk of 0x657350 ItaSerC2b::ItaSerC2b with no own frame, ends with its epilogue, ret 8 | Error exit of the Serie C2 group B constructor that formats the versioned assert text, shows the error box and returns this. | medium | opus |  |
| 0x657580 | 11 | `ItaSerC2b::`scalar deleting destructor'` | thiscall(ItaSerC2b* this, unsigned flags) ret 4, returns this | Runs the Serie C2 group B destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x6575a0 | 57 (+1 unwind) | `ItaSerC2b::~ItaSerC2b` | thiscall(ItaSerC2b* this) ret 0 | Destroys the Serie C2 group B league by freeing its table, schedule, play-off stages and stats, then runs the League destructor. | high | opus |  |
| 0x657660 | 927 | `ItaSerC2b::create_schedule` | thiscall(ItaSerC2b* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns schedule pointer or null | Builds the 34-round league schedule for stage -1, the two-round promotion play-off for stage 0 and the two-leg relegation play-out for stage 1. | high | opus |  |
| 0x657f50 | 84 | `ItaSerC2b::init_team_list` | thiscall(ItaSerC2b* this) ret 0, returns bool | Sets the team count to 18, allocates the league table and fills one row for each club whose division is Serie C2 group B. | high | opus |  |
| 0x658050 | 43 | `ItaSerC2b::set_up_rules` | thiscall(ItaSerC2b* this) ret 0, returns 1 | Sets the points, promotion, play-off and relegation counts of Serie C2 group B, links the sibling groups and builds the league schedule. | high | opus |  |
| 0x658100 | 143 | `ItaSerC2b::start_new_season` | thiscall(ItaSerC2b* this) ret 0 | Clears the finished Serie C2 group B season, archives its stats, moves the year on and builds the rules, table and fixtures again. | high | opus |  |
| 0x6582c0 | 40 | `ItaSerC2b::advance_stage` | thiscall(ItaSerC2b* this) ret 0 | Moves the stage counter on and builds the play-off stages at stage 0, or asserts when it passes the last stage. | high | opus |  |
| 0x658350 | 223 (+2 unwind) | `ItaSerC2b::create_playoff_stages` | thiscall(ItaSerC2b* this) ret 0 | Builds the promotion play-off Cup_Stage for table places 2 to 5 and the relegation play-out Cup_Stage for places 14 to 17. | high | opus |  |
| 0x658640 | 65 | `ItaSerC2b::set_club_progress` | thiscall(ItaSerC2b* this, Club* club, char stage, char current, char best, char worst) ret 0x14 | Maps the play-off stage codes of a club to league position codes and writes the three progress bytes of its Comp_Stats entry. | high | opus |  |
| 0x658750 | 2861 (+1 unwind) | `ItaSerC2b::load_fixed_fixtures` | thiscall(ItaSerC2b* this) ret 0 | Allocates the fixed fixture table and enters the real 2001 to 2002 Serie C2 group B fixtures by club name and date. | high | opus | 2026-10-16-sweep-season-end.md |
