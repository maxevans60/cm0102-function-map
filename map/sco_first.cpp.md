# sco_first.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7edfc0 | 169 (+2 unwind) | `ScoFirst::ScoFirst` | thiscall(ScoFirst* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Scottish First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x7ee200 | 11 | `ScoFirst::`scalar deleting destructor'` | thiscall(ScoFirst* this, unsigned flags) ret 4, returns this | Runs the Scottish First Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7ee220 | 60 (+1 unwind) | `ScoFirst::~ScoFirst` | thiscall(ScoFirst* this) ret 0 | Destroys the Scottish First Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7ee2e0 | 1042 | `ScoFirst::create_schedule` | thiscall(ScoFirst* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 36-round schedule of the Scottish First Division from August for stage -1, or the three-round play-off group schedule for stage 0. | high | opus |  |
| 0x7eed30 | 95 | `ScoFirst::create_table` | thiscall(ScoFirst* this) ret 0, returns 1 on success and 0 on failure | Allocates the ten-row table, fills it with the clubs of the Scottish First Division and sets the prize fund. | high | opus |  |
| 0x7eee50 | 46 | `ScoFirst::set_up_rules` | thiscall(ScoFirst* this) ret 0, returns 1 | Sets the First Division rules with the Premier Division above and Second Division below, one direct promotion place, and builds the schedule. | high | opus |  |
| 0x7eef00 | 162 | `ScoFirst::start_new_season` | thiscall(ScoFirst* this) ret 0 | Frees last season's table, schedule and stages, archives the stats, advances the year, then rebuilds rules, table and fixtures and renews officials. | high | opus |  |
| 0x7ef100 | 133 | `ScoFirst::set_club_progress` | thiscall(ScoFirst* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | In the 1999 season stores a club's three progress codes in its stats entry with play-off codes remapped, otherwise forwards to Comp::set_club_progress. | high | opus |  |
| 0x7ef270 | 59 | `ScoFirst::advance_stage` | thiscall(ScoFirst* this) ret 0 | Once the Premier Division is complete, updates its positions, moves the stage counter on and creates the play-off group at the first stage. | high | opus |  |
| 0x7ef340 | 201 (+1 unwind) | `ScoFirst::create_playoff_group` | thiscall(ScoFirst* this) ret 0 | Builds a three-club play-off group League_Stage from the two First Division clubs in play-off places and the Premier Division club in its play-off place. | high | opus |  |
| 0x7ef5d0 | 182 | `ScoFirst::update_staff_records_for_status` | thiscall(ScoFirst* this, Club* club, char status, char stage, ...) ret 0x18, returns division id or 0 | Updates staff records for a club's final status, and in the play-off marks First and Premier Division clubs as promoted, staying or relegated. | high | opus |  |
| 0x7ef7c0 | 179 | `ScoFirst::build_fate_news_text` | thiscall(ScoFirst* this, int club_index, char fate, char cup_flag, ..., int comp_id, ..., int playoff, ...) ret 0x28 | Builds the news text for a club's play-off group outcome, such as promotion, avoiding relegation or relegation, else uses the base Comp text. | high | opus |  |
