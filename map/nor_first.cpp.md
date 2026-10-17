# nor_first.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x78fd40 | 159 (+2 unwind) | `NorFirst::NorFirst` | thiscall(NorFirst* this, short year, Division* division) ret 8, returns this | Constructs the Norwegian First Division on League, then loads saved data or sets up rules, table, fixtures, sorting and its Comp_Stats object. | high | opus |  |
| 0x78ff60 | 11 | `NorFirst::`scalar deleting destructor'` | thiscall(NorFirst* this, unsigned flags) ret 4, returns this | Runs the NorFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x78ff80 | 60 (+1 unwind) | `NorFirst::~NorFirst` | thiscall(NorFirst* this) ret 0 | Destroys the Norwegian First Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x790040 | 939 (+4 unwind) | `NorFirst::create_schedule` | thiscall(NorFirst* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 26-round or 30-round league schedule from April for stage -1, or the one-round play-off cup template in October for stage 0. | high | opus |  |
| 0x7909a0 | 107 | `NorFirst::create_table` | thiscall(NorFirst* this) ret 0, returns true when the table fills | Allocates the table, counts the clubs of the Norwegian First Division and fills 16 rows, or 14 rows when only 14 clubs exist. | high | opus |  |
| 0x790b00 | 38 | `NorFirst::set_up_rules` | thiscall(NorFirst* this) ret 0, returns 1 | Sets the Norwegian First Division rule bytes, with the Premier Division above and no lower league, and builds the base schedule. | high | opus |  |
| 0x790b90 | 143 | `NorFirst::start_new_season` | thiscall(NorFirst* this) ret 0 | Archives the season, deletes the old stages and rebuilds rules, table, fixtures and predicted positions, then reviews managers and renews officials. | high | opus |  |
| 0x790d50 | 59 | `NorFirst::advance_stage` | thiscall(NorFirst* this) ret 0 | Moves to the next stage once the Premier Division is complete, and builds the promotion play-off stage when the stage index reaches 0. | high | opus |  |
| 0x790e20 | 191 (+1 unwind) | `NorFirst::create_play_off_stage` | thiscall(NorFirst* this) ret 0 | Builds stage 0, a two-club tie between the First Division club with play-off status and the Premier Division club with play-off status. | high | opus |  |
| 0x791080 | 180 | `NorFirst::update_staff_records_for_status` | thiscall(NorFirst* this, Club* club, char status, char stage, int arg4, int arg5, int arg6) ret 0x18, returns comp id or 0 | Adds staff history records for the league champion, play-off and relegated clubs, and sets table status bytes after the promotion play-off. | high | opus |  |
| 0x791270 | 136 | `NorFirst::build_fate_news_text` | thiscall(NorFirst* this, int club_index, char fate, char stage, int a4, int a5, int a6, int comp_id, int a8, int has_partner, int a10) ret 0x28 | Writes news that a club avoids relegation or goes down from the Premier Division, or wins promotion, after the play-off, else defers to Comp. | high | opus |  |
| 0x7913f0 | 98 | `NorFirst::set_club_progress` | thiscall(NorFirst* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, mapping play-off results to codes 11 and 14 for Premier Division clubs. | high | opus |  |
