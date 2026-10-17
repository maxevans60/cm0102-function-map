# ita_ser_c1a.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x64aa70 | 161 (+2 unwind) | `ItaSerC1a::ItaSerC1a` | thiscall(ItaSerC1a* this, short year, CompRecord* comp) ret 8, returns this | Constructs Serie C1/A on League with two play-off stages and, when no saved data loads, sets up rules, table, fixed fixtures, fixtures and Comp_Stats. | high | opus |  |
| 0x64aca0 | 11 | `ItaSerC1a::`scalar deleting destructor'` | thiscall(ItaSerC1a* this, unsigned flags) ret 4, returns this | Runs the Serie C1/A destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x64acc0 | 57 (+1 unwind) | `ItaSerC1a::~ItaSerC1a` | thiscall(ItaSerC1a* this) ret 0 | Destroys Serie C1/A by freeing its table, schedule, play-off stage objects, stage array and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x64ad80 | 927 | `ItaSerC1a::create_schedule` | thiscall(ItaSerC1a* this, char stage, short* round_count, short* extra, int* out_flag) ret 0x10, returns schedule pointer or null | Builds the 34-round league template for stage -1, the two-round promotion play-off for stage 0 and the one-round relegation play-out for stage 1. | high | opus |  |
| 0x64b670 | 84 | `ItaSerC1a::create_table` | thiscall(ItaSerC1a* this) ret 0, returns 1 on success and 0 on failure | Allocates the 18-row table and fills it with the clubs of Serie C1/A. | high | opus |  |
| 0x64b770 | 43 | `ItaSerC1a::set_up_rules` | thiscall(ItaSerC1a* this) ret 0, returns 1 | Sets the Serie C1/A rule bytes with four play-off clubs, links Serie B above and builds the stage -1 schedule. | high | opus |  |
| 0x64b820 | 143 | `ItaSerC1a::start_new_season` | thiscall(ItaSerC1a* this) ret 0 | Frees the old table, schedule and play-off stages, archives the stats, moves the year on and rebuilds rules, table, fixtures and sorted table. | high | opus |  |
| 0x64b9e0 | 40 | `ItaSerC1a::advance_stage` | thiscall(ItaSerC1a* this) ret 0 | Moves the stage index on by one and creates both play-off stages when it reaches 0, or reports an error past the last stage. | high | opus |  |
| 0x64ba70 | 237 (+2 unwind) | `ItaSerC1a::create_playoff_stages` | thiscall(ItaSerC1a* this) ret 0 | Enters the champion in the Serie C1 Super Cup, then builds the play-off for places 2 to 5 and the play-out for 14 to 17. | high | opus |  |
| 0x64bd80 | 65 | `ItaSerC1a::set_club_progress` | thiscall(ItaSerC1a* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, grouping play-off places 2 to 5 and play-out places 14 to 17. | high | opus |  |
| 0x64be90 | 2861 (+1 unwind) | `ItaSerC1a::set_up_fixed_fixtures` | thiscall(ItaSerC1a* this) ret 0 | Builds the real 2001/02 Serie C1/A fixture list by club name and drops it when any club is missing. | high | opus | 2026-10-16-sweep-season-end.md |
