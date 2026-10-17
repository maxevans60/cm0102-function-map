# ita_ser_b.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x645810 | 160 (+2 unwind) | `ItaSerB::ItaSerB` | thiscall(ItaSerB* this, short year, CompRecord* comp) ret 8, returns this | Constructs Serie B on League and, when no saved data loads, sets up rules, the 20-club table, fixed fixtures, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x645a40 | 11 | `ItaSerB::`scalar deleting destructor'` | thiscall(ItaSerB* this, unsigned flags) ret 4, returns this | Runs the Serie B destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x645a60 | 38 (+1 unwind) | `ItaSerB::~ItaSerB` | thiscall(ItaSerB* this) ret 0 | Destroys Serie B by freeing its table, schedule template and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x645af0 | 1445 | `ItaSerB::create_schedule` | thiscall(ItaSerB* this, char stage, short* round_count, short* extra, int* out_flag) ret 0x10, returns schedule pointer or null | Builds the 38-round league template for stage -1, or the one-round tiebreak play-off table sized by the play-off pair count for stage 0. | high | opus |  |
| 0x646780 | 95 | `ItaSerB::create_table` | thiscall(ItaSerB* this) ret 0, returns 1 on success and 0 on failure | Allocates the 20-row table, fills it with the clubs of Serie B and sets a prize fund from 70000. | high | opus |  |
| 0x6468a0 | 45 | `ItaSerB::set_up_rules` | thiscall(ItaSerB* this) ret 0, returns 1 | Sets the Serie B rule bytes, links Serie A above and Serie C1/A below, enables the tiebreak check and builds the stage -1 schedule. | high | opus |  |
| 0x646920 | 19 | `ItaSerB::set_up_rules_fragment_646920` | not a function entry: body fragment of 0x6468a0 sharing its frame, ret 0 | Repeats the tail of set_up_rules that stores the last rule bytes and builds the stage -1 schedule, read as a separate entry. | high | opus |  |
| 0x646960 | 135 | `ItaSerB::start_new_season` | thiscall(ItaSerB* this) ret 0 | Frees the old table and schedule, archives the stats, moves the year on and rebuilds rules, table, fixtures and sorted table. | high | opus |  |
| 0x646b20 | 40 | `ItaSerB::advance_stage` | thiscall(ItaSerB* this) ret 0 | Moves the stage index on by one and creates the tiebreak play-off stage when it reaches 0, or reports an error past the last stage. | high | opus |  |
| 0x646b50 | 19 | `ItaSerB::advance_stage_fragment_646b50` | not a function entry: body fragment of 0x646b20 sharing its frame, ret 0 | Repeats the error report of advance_stage that shows the version and assert line in an Error box, read as a separate entry. | high | opus |  |
| 0x646bb0 | 212 (+1 unwind) | `ItaSerB::create_tiebreak_playoff_stage` | thiscall(ItaSerB* this) ret 0 | Pairs adjacent clubs level on points across a title, promotion or relegation boundary and builds a Cup_Stage of those play-off ties. | high | opus |  |
| 0x646c50 | 176 | `ItaSerB::create_tiebreak_playoff_stage_fragment_646c50` | not a function entry: body fragment of 0x646bb0 sharing its frame, ret 0 | Repeats the pairing loop and Cup_Stage creation of create_tiebreak_playoff_stage, read as a separate entry from inside that function. | high | opus |  |
| 0x646e6f | 1 | `ita_ser_b_nop_pad_646e6f` | not a function entry: one nop alignment byte that falls through into 0x646e70 | Pads the code before ItaSerB::update_staff_records_for_status and holds no code of its own. | high | opus |  |
| 0x646e70 | 149 | `ItaSerB::update_staff_records_for_status` | thiscall(ItaSerB* this, Club* club, char status, char stage, int a4, Fixture* match, int a6) ret 0x18 | Passes league results to the base, and for a tiebreak winner moves the club above its opponent and ends the season when no tie remains. | high | opus |  |
| 0x647050 | 104 | `ItaSerB::update_for_date` | thiscall(ItaSerB* this, Date* today, int full_update) ret 8, returns base result | Runs the daily league tasks and, when the season ends with clubs level on points across a zone boundary, starts a tiebreak play-off stage. | high | opus |  |
| 0x6471a0 | 48 | `ita_league_sort_clubs_level_on_points` | thiscall(League* this, short points) ret 4 | Ranks the table by head to head, sorts the rows of clubs on the given points and renumbers every table position. | high | opus |  |
| 0x647230 | 3527 (+1 unwind) | `ItaSerB::set_up_fixed_fixtures` | thiscall(ItaSerB* this) ret 0 | Builds the real 2001/02 Serie B fixture list by club name and drops it when any club is missing. | high | opus | 2026-10-16-sweep-season-end.md |
