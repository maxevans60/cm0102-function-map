# pol_second.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7cb1d0 | 159 (+2 unwind) | `PolSecond::PolSecond` | thiscall(PolSecond* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Polish Second Division on League, loads it from the temp file or sets rules, fills the table, makes fixtures and creates Comp_Stats. | high | opus |  |
| 0x7cb3f0 | 11 | `PolSecond::`scalar deleting destructor'` | thiscall(PolSecond* this, unsigned flags) ret 4, returns this | Runs the Polish Second Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7cb410 | 38 (+1 unwind) | `PolSecond::~PolSecond` | thiscall(PolSecond* this) ret 0 | Destroys the Polish Second Division by freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7cb4a0 | 990 | `PolSecond::create_schedule` | thiscall(PolSecond* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 34-round season template, or 38 rounds in 2001, for stage -1 and the one-round promotion play-off cup for stage 0. | high | opus |  |
| 0x7cbdf0 | 104 | `PolSecond::create_table` | thiscall(PolSecond* this) ret 0, returns 1 on success and 0 on failure | Allocates the 18-row table, or 20 rows in 2001, fills it with the Polish Second Division clubs and sets the prize fund. | high | opus |  |
| 0x7cbf40 | 43 | `PolSecond::set_up_rules` | thiscall(PolSecond* this) ret 0, returns 1 | Sets the Polish Second Division rule bytes with two stages and the First Division above and no division below, then builds the schedule. | high | opus |  |
| 0x7cc000 | 143 | `PolSecond::start_new_season` | thiscall(PolSecond* this) ret 0 | Frees the old table, schedule and stages, archives Comp_Stats, increments the year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x7cc1c0 | 61 | `PolSecond::advance_stage` | thiscall(PolSecond* this) ret 0 | Moves to the play-off stage once the Polish First Division is complete, building the promotion play-off, or reports an error past the last stage. | high | opus |  |
| 0x7cc290 | 171 (+1 unwind) | `PolSecond::create_play_off_stage` | thiscall(PolSecond* this) ret 0 | Pairs two Second Division clubs with play-off status against two First Division clubs and creates the play-off Cup_Stage as stage 0. | high | opus |  |
| 0x7cc490 | 182 | `PolSecond::update_staff_records_for_status` | thiscall(PolSecond* this, Club* club, char result, char stage, int a4, Fixture* match, int a6) ret 0x18, returns comp id or 0 | Adds staff records for title, play-off and relegation outcomes, and sets the table status of both play-off clubs after the play-off. | high | opus |  |
| 0x7cc680 | 136 | `PolSecond::build_fate_news_text` | thiscall(PolSecond* this, int club_index, char fate, char stage, int a4, int a5, int a6, int comp_id, int a8, int full_sentence, int a10) ret 0x28 | Writes the play-off news text for a club that avoids relegation, wins promotion or goes down, deferring other cases to the Comp base. | high | opus |  |
| 0x7cc800 | 102 | `PolSecond::set_club_progress` | thiscall(PolSecond* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, remapping them for the season and for First Division clubs in the play-off. | high | opus |  |
