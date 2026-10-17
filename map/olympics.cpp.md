# olympics.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x79f530 | 121 (+2 unwind) | `Olympics::Olympics` | thiscall(Olympics* this, short year, int nation) ret 8, returns this | Constructs the Olympic football league, rounds the year up to an Olympic year, loads saved data or sets up rules and statistics. | high | opus | 2026-10-16-sweep-international.md |
| 0x79f6f0 | 11 | `Olympics::`scalar deleting destructor'` | thiscall(Olympics* this, unsigned flags) ret 4, returns this | Runs the Olympics destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x79f710 | 60 (+1 unwind) | `Olympics::~Olympics` | thiscall(Olympics* this) ret 0 | Destroys the Olympics league, freeing the table, the schedule, each group and knockout stage, the statistics and the League base. | high | opus |  |
| 0x79f7d0 | 585 | `Olympics::create_schedule` | thiscall(Olympics* this, char stage, short* round_count, short* stage_id, int* is_league) ret 0x10, returns schedule pointer | Builds the round template for a stage, three group rounds for stages 0 to 2 or four knockout rounds for stage 3. | high | opus |  |
| 0x79fea0 | 234 | `Olympics::build_fate_news_text` | thiscall(Olympics* this, int club_index, char fate, char stage, ..., int cup_result, ...) ret 0x28 | Writes the news text for a nation that qualifies from its group, wins, finishes in a top four place, goes through or is knocked out. | high | opus |  |
| 0x7a0140 | 66 | `Olympics::init_group_a_table` | thiscall(Olympics* this) ret 0, returns int | Sets the league to four teams, builds its table from the first four drawn finalists and posts the group draw news. | medium | opus |  |
| 0x7a0230 | 54 (+1 unwind) | `Olympics::set_up_rules` | thiscall(Olympics* this) ret 0, returns int | Sets the Olympic points, match and draw date rules, then creates the schedule for the group stage. | high | opus |  |
| 0x7a0300 | 122 | `Olympics::update_staff_records_for_status` | thiscall(Olympics* this, Club* club, char status, char stage, int arg4, Fixture* fixture, int arg6) ret 0x18 | Writes staff records for a nation's group qualification or failure and for progress, elimination, win or runner-up in the knockout stage. | high | opus |  |
| 0x7a0450 | 74 | `Olympics::start_new_season` | thiscall(Olympics* this) ret 0 | Clears the table, archives statistics, deletes all stages, moves the year on by four and sets up the rules again. | high | opus |  |
| 0x7a0540 | 40 | `Olympics::advance_stage` | thiscall(Olympics* this) ret 0 | Moves the stage counter on, asserts when it passes the last stage and creates the knockout stage when the counter reaches 3. | high | opus |  |
| 0x7a05d0 | 149 (+1 unwind) | `Olympics::create_group_stage` | thiscall(Olympics* this, int group_index) ret 4, returns int | Creates a League_Stage of four teams for group B, C or D from the drawn pool and posts the group draw news. | high | opus |  |
| 0x7a07c0 | 160 (+1 unwind) | `Olympics::create_knockout_stage` | thiscall(Olympics* this) ret 0 | Builds the eight quarter-finalists from the top two places of the four groups and creates the knockout Cup_Stage. | high | opus |  |
| 0x7a09e0 | 605 | `Olympics::draw_finalists` | thiscall(Olympics* this) ret 0, returns int | Fills the sixteen finalist slots with national under-21 teams, a fixed list for 2000 or hosts plus continental quotas otherwise. | medium | opus |  |
| 0x7a11c0 | 155 (+2 unwind) | `Olympics::update_for_date` | thiscall(Olympics* this, Date* today, int full_update) ret 8, returns int | On the draw date runs the finalist draw, predicted positions, the group A table, fixtures and groups B to D, then runs the base update. | high | opus |  |
| 0x7a13e0 | 169 | `Olympics::set_predicted_positions` | thiscall(Olympics* this) ret 0 | Sorts the sixteen finalists and sets their predicted final positions as 1, 2, 3, 3, then 5, 9 and 13 in fours. | high | opus |  |
| 0x7a15d0 | 65 | `Olympics::set_club_progress` | thiscall(Olympics* this, Club* club, char stage, char code_a, char code_b, char code_c) ret 0x14 | Maps group stage progress codes to tournament codes and writes the three progress bytes of a club's statistics entry. | high | opus |  |
