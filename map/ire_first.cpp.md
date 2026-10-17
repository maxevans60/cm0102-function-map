# ire_first.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x634c40 | 159 (+2 unwind) | `IreFirst::IreFirst` | thiscall(IreFirst* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Irish First Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x634d20 | 28 | `IreFirst::IreFirst_fragment_634d20` | none, false entry inside 0x634c40, ret 8 | Marks a false function start inside the IreFirst constructor, on the shared path that formats and shows the assertion message box. | high | opus |  |
| 0x634e60 | 11 | `IreFirst::`scalar deleting destructor'` | thiscall(IreFirst* this, unsigned flags), returns this, ret 4 | Runs the IreFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x634e80 | 60 (+1 unwind) | `IreFirst::~IreFirst` | thiscall(IreFirst* this), ret 0 | Destroys the Irish First Division, freeing its table, schedule, play-off stages and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x634f40 | 995 (+3 unwind) | `IreFirst::create_schedule` | thiscall(IreFirst* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 34 or 36 round league schedule from August to April for stage -1, or the one-round two-leg play-off for stage 0. | high | opus |  |
| 0x635420 | 422 | `IreFirst::create_schedule_fragment_635420` | none, false entry inside 0x634f40, ret 0x10 | Marks a false function start inside IreFirst::create_schedule, where the December and spring rounds are dated and the round count is checked. | high | opus |  |
| 0x635910 | 123 | `IreFirst::create_table` | thiscall(IreFirst* this), returns true when the table is full, ret 0 | Counts the clubs of the Irish First Division, sets three or four league cycles and fills one table row a club. | high | opus |  |
| 0x635aa0 | 41 | `IreFirst::set_up_rules` | thiscall(IreFirst* this), returns 1, ret 0 | Sets the Irish First Division rule bytes, with the Premier Division above and no lower league, and builds the schedule for stage -1. | high | opus |  |
| 0x635b30 | 143 | `IreFirst::start_new_season` | thiscall(IreFirst* this), ret 0 | Frees last season's table, schedule and play-off stages, archives the statistics, then rebuilds rules, table and fixtures for the new year. | high | opus |  |
| 0x635cf0 | 59 | `IreFirst::advance_stage` | thiscall(IreFirst* this), ret 0 | Waits for the Irish Premier Division to finish, updates its positions and starts the promotion play-off stage once. | high | opus |  |
| 0x635dc0 | 191 (+1 unwind) | `IreFirst::create_promotion_playoff_stage` | thiscall(IreFirst* this), ret 0 | Pairs the First Division club in the play-off place with the Premier Division play-off club and builds a two-team cup stage for them. | high | opus |  |
| 0x636020 | 179 | `IreFirst::update_staff_records_for_status` | thiscall(IreFirst* this, Club* club, char status, char stage), returns the club's new division id or 0, ret 0x18 | Writes staff records for league status changes, and after the play-off promotes the First Division winner and relegates the Premier loser. | high | opus |  |
| 0x636150 | 1 | `IreFirst::update_staff_records_for_status_fragment_636150` | none, false entry inside 0x636020, ret 0x18 | Marks a false function start on the final ret 0x18 of IreFirst::update_staff_records_for_status, which its branches jump to. | high | opus |  |
| 0x636210 | 136 | `IreFirst::build_fate_news_text` | thiscall-style ret 0x28 (int club_index, char fate, char cup_result, ..., int comp_id, ..., int full_sentence, ...) | Builds the play-off news text, saying the Premier club avoids relegation or is relegated and the First Division club wins promotion. | high | opus |  |
| 0x636390 | 98 | `IreFirst::set_club_progress` | thiscall-style ret 0x14 (Club* club, char stage, char code1, char code2, char code3) | Stores the three progress codes of a club in its Comp_Stats entry, remapping them for the league stage and the promotion play-off. | high | opus |  |
