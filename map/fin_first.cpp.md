# fin_first.cpp: 19 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x592eb0 | 161 (+2 unwind) | `FinFirst::FinFirst` | thiscall(FinFirst* this, short year, CompRecord* comp_record), returns this, ret 8 | Constructs the Finnish First Division with its rules, North group table, fixtures, Comp_Stats object and South group stage. | high | opus |  |
| 0x5930e0 | 11 | `FinFirst::`scalar deleting destructor'` | thiscall(FinFirst* this, unsigned flags), returns this, ret 4 | Runs the FinFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x593100 | 60 (+1 unwind) | `FinFirst::~FinFirst` | thiscall(FinFirst* this), ret 0 | Frees the table, the base schedule, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x5931c0 | 865 | `FinFirst::create_schedule` | thiscall(FinFirst* this, char stage, short* round_count, short* comp_code, int* is_league), returns schedule template, ret 0x10 | Builds the round dates of the 27-round group league or the cup round templates of the three play-off stages. | high | opus |  |
| 0x593a70 | 91 | `FinFirst::create_table` | thiscall(FinFirst* this), returns bool, ret 0 | Allocates the 10-row table and fills it with the clubs of the Finnish First Division North group. | high | opus |  |
| 0x593b80 | 39 | `FinFirst::set_up_rules` | thiscall(FinFirst* this), returns 1, ret 0 | Sets the league rules of the Finnish First Division and builds the base league schedule. | high | opus |  |
| 0x593c20 | 159 | `FinFirst::start_new_season` | thiscall(FinFirst* this), ret 0 | Archives the season, deletes the old stages and rebuilds the rules, North table, fixtures and South group stage for the new season. | high | opus |  |
| 0x593e10 | 136 | `FinFirst::set_club_progress` | thiscall(FinFirst* this, Club* club, char stage, char code_a, char code_b, char code_c), this unused, ret 0x14 | Writes a club's three progress codes in its Comp_Stats entry, mapping play-off results to codes 11 and 12 or 15 and 17. | high | opus |  |
| 0x593f90 | 70 | `FinFirst::advance_stage` | thiscall(FinFirst* this), ret 0 | Moves to the next stage, building the play-off stages after the groups and the Premier Division play-off once that league is complete. | high | opus |  |
| 0x594080 | 475 (+2 unwind) | `FinFirst::create_play_off_stages` | thiscall(FinFirst* this), ret 0 | Picks four Second Division clubs for promotion, then builds the promotion play-off stage 1 and the relegation play-off stage 2. | medium | opus |  |
| 0x594610 | 157 (+1 unwind) | `FinFirst::create_premier_play_off_stage` | thiscall(FinFirst* this), ret 0 | Builds stage 3, a two-club tie between the First Division play-off winner and the Premier Division play-off club. | high | opus |  |
| 0x594810 | 189 | `FinFirst::update_staff_records_for_status` | thiscall(FinFirst* this, Club* club, char status, char stage, ...), returns comp id or 0, ret 0x18 | Adds staff history records and sets table status bytes for group winners, play-off qualifiers, relegated clubs and Premier play-off results. | high | opus |  |
| 0x594850 | 28 | `FinFirst::update_staff_records_for_status_fragment_594850` | none, false entry inside 0x594810, ret 0x18 | Marks a false function start inside update_staff_records_for_status, where a club row in either group gets status byte 5. | medium | opus |  |
| 0x594a10 | 236 | `FinFirst::build_fate_news_text` | thiscall(FinFirst* this, int club_index, char fate, char stage, int a4, int a5, int a6, int comp_id, int a8, int full_sentence, int a10), ret 0x28 | Writes news that a club qualifies for the play-offs, avoids relegation, goes down or wins promotion, and defers other fates to the Comp base. | high | opus |  |
| 0x594cd0 | 222 (+1 unwind) | `FinFirst::create_south_group_stage` | thiscall(FinFirst* this), ret 0 | Collects the ten Finnish First Division South clubs and builds the League_Stage of that group as stage 0. | high | opus |  |
| 0x594fb0 | 10 | `FinFirst::load_extra_data` | thiscall(FinFirst* this, FILE* file), returns 1, ret 4 | Reads the four stored Second Division club ids at +0xee from the saved game file. | high | opus |  |
| 0x594fd0 | 9 | `FinFirst::save_extra_data` | thiscall(FinFirst* this, FILE* file), ret 4 | Writes the four stored Second Division club ids at +0xee to the saved game file. | high | opus |  |
| 0x594ff0 | 122 | `FinFirst::set_predicted_positions` | thiscall(FinFirst* this), ret 0 | Sorts the clubs of the North table and the South group stage and gives them alternating predicted positions in Comp_Stats. | high | opus |  |
| 0x595160 | 4 | `FinFirst::record_season_honours` | thiscall(FinFirst* this), tail jump, no own ret | Forwards the season honours to slot 12 of the second stage object by a tail jump. | high | opus |  |
