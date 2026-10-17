# ita_ser_c1b.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x64ec20 | 161 (+2 unwind) | `ItaSerC1b::ItaSerC1b` | thiscall(ItaSerC1b* this, short year, void* comp_record) ret 8, returns this | Constructs the Serie C1 group B league on League and, when no saved data loads, sets its rules, table, fixed fixtures, fixtures and stats. | high | opus |  |
| 0x64ee50 | 11 | `ItaSerC1b::`scalar deleting destructor'` | thiscall(ItaSerC1b* this, unsigned flags) ret 4, returns this | Runs the ItaSerC1b destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x64ee70 | 57 (+1 unwind) | `ItaSerC1b::~ItaSerC1b` | thiscall(ItaSerC1b* this) ret 0 | Restores the ItaSerC1b vtable, frees the table, schedule, play-off stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x64ef30 | 927 | `ItaSerC1b::create_schedule` | thiscall(ItaSerC1b* this, char stage, short* round_count, short* stage_id, int* is_league) ret 0x10, returns schedule pointer or null | Builds the 34-round league schedule for stage -1, the two-round promotion play-off for stage 0 and the one-round play-out for stage 1. | high | opus |  |
| 0x64f820 | 84 | `ItaSerC1b::create_table` | thiscall(ItaSerC1b* this) ret 0, returns 1 when all 18 rows fill | Allocates the 18-row league table and fills it with the clubs whose division is the Serie C1 group B competition. | high | opus |  |
| 0x64f920 | 51 | `ItaSerC1b::set_up_rules` | thiscall(ItaSerC1b* this) ret 0, returns 1 | Sets the league rule bytes, the league above, the league below when the nation plays Serie C2, then builds the schedule. | high | opus |  |
| 0x64f9e0 | 143 | `ItaSerC1b::start_new_season` | thiscall(ItaSerC1b* this) ret 0 | Frees last season's table, schedule and play-off stages, archives the stats, moves the year on and rebuilds rules, table and fixtures. | high | opus |  |
| 0x64fba0 | 40 | `ItaSerC1b::advance_stage` | thiscall(ItaSerC1b* this) ret 0 | Moves the stage counter on, reports an error after the last stage and builds the play-off stages when stage 0 starts. | high | opus |  |
| 0x64fc30 | 237 (+2 unwind) | `ItaSerC1b::create_play_off_stages` | thiscall(ItaSerC1b* this) ret 0 | Enters the champion in the C1 Super Cup, then builds the promotion play-off for places 2 to 5 and the play-out for 14 to 17. | high | opus |  |
| 0x64ff40 | 65 | `ItaSerC1b::set_club_progress` | thiscall(ItaSerC1b* this, Club* club, char stage, char current, char best, char worst) ret 0x14 | Folds league places 2 to 5 and 14 to 17 into play-off codes and stores the current, best and worst progress in the club stats. | high | opus |  |
| 0x650050 | 60 | `ItaSerC1b::record_final_positions` | thiscall(ItaSerC1b* this), ret 0 | Stores each club's previous division and final place from the table, then sets places 2 onwards from the play-off stage result. | high | opus |  |
| 0x650100 | 2861 (+1 unwind) | `ItaSerC1b::set_up_fixed_fixtures` | thiscall(ItaSerC1b* this) ret 0 | Allocates the fixed fixture array and fills it with the real 2001/02 Serie C1 group B fixtures by club name. | high | opus | 2026-10-16-sweep-season-end.md |
