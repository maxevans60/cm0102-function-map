# tur_second_b.cpp: 19 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8ff4c0 | 168 (+2 unwind) | `TurSecondB::TurSecondB` | thiscall(TurSecondB* this, short comp_id, CompRecord* comp) ret 8, returns this | Builds the Turkish second division B league, then loads it from the temp file or sets up rules, table, fixtures and group stages. | high | opus |  |
| 0x8ff700 | 11 | `TurSecondB::`scalar deleting destructor'` | thiscall(TurSecondB* this, unsigned flags) ret 4, returns this | Runs the TurSecondB destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x8ff720 | 60 (+1 unwind) | `TurSecondB::~TurSecondB` | thiscall(TurSecondB* this) ret 0 | Restores the TurSecondB vtable, frees the table, schedule, stage objects and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x8ff7e0 | 1070 | `TurSecondB::create_schedule` | thiscall(TurSecondB* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the round dates and match slots of the schedule for one stage of the Turkish second division B season. | high | opus |  |
| 0x9002c0 | 126 | `TurSecondB::create_table` | thiscall(TurSecondB* this) ret 0, returns 1 when all 10 rows fill | Allocates the 10 row league table and fills it with the clubs whose division is this league and whose group is the first group. | high | opus |  |
| 0x900460 | 38 | `TurSecondB::set_up_rules` | thiscall(TurSecondB* this) ret 0, returns 1 | Sets the points, tie break and promotion rules of the league, then builds its schedule through the create_schedule slot. | high | opus |  |
| 0x900500 | 147 | `TurSecondB::start_new_season` | thiscall(TurSecondB* this) ret 0 | Archives the old season, deletes the stages, then rebuilds rules, table, fixtures and the four group stages for the new season. | high | opus |  |
| 0x9006c0 | 54 | `TurSecondB::advance_stage` | thiscall(TurSecondB* this) ret 0 | Moves to the next stage and builds the promotion and classification groups at stage 4 or the playoff at stage 10. | high | opus |  |
| 0x900780 | 239 (+1 unwind) | `TurSecondB::create_group_stage` | thiscall(TurSecondB* this, char group) ret 4 | Collects the 10 clubs of one regional group and creates its League_Stage as stage 0 to 3. | high | opus |  |
| 0x900ab0 | 175 (+1 unwind) | `TurSecondB::create_promotion_group` | thiscall(TurSecondB* this) ret 0 | Takes the qualified clubs of the five first phase tables and creates the 10 club promotion group as stage 4. | medium | opus |  |
| 0x900d00 | 238 (+1 unwind) | `TurSecondB::create_classification_groups` | thiscall(TurSecondB* this) ret 0 | Creates five 8 club groups, stages 5 to 9, from the clubs that did not qualify and carries over their first phase records. | medium | opus |  |
| 0x901040 | 191 (+1 unwind) | `TurSecondB::create_playoff_stage` | thiscall(TurSecondB* this) ret 0 | Builds the 8 club playoff cup stage from the qualified promotion group clubs and the five classification group winners. | medium | opus |  |
| 0x9012d0 | 233 | `TurSecondB::update_staff_records_for_status` | thiscall(TurSecondB* this, Club* club, char status, char stage, ...) ret 0x18 | Records group qualification, promotion, relegation and playoff results in staff records and sets the row status flag per stage. | high | opus |  |
| 0x9015f0 | 183 | `TurSecondB::build_fate_news_text` | thiscall(TurSecondB* this, int club_index, char fate, char stage, ..., int full_sentence, ...) ret 0x28 | Writes the promotion news for the promotion group and the playoff qualification news for the classification groups, else uses the base text. | high | opus |  |
| 0x901800 | 95 | `TurSecondB::get_club_array` | thiscall(TurSecondB* this, Club*** out_clubs, short* out_count) ret 8 | Allocates an array of the 50 clubs of this table and the four group stages and returns it with the count. | high | opus |  |
| 0x901950 | 123 | `TurSecondB::set_predicted_positions` | thiscall(TurSecondB* this) ret 0 | Sorts the clubs of each of the five first phase tables by strength and stores each rank as a predicted position. | high | opus |  |
| 0x901ac0 | 78 | `TurSecondB::set_club_progress` | thiscall(TurSecondB* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Maps a club's stage codes to the overall season codes for each stage and stores them in its Comp_Stats entry. | high | opus |  |
| 0x901ba0 | 66 | `TurSecondB::record_final_positions` | thiscall(TurSecondB* this) ret 0 | Stores this league and a final position in each club, 1 and 2 for group qualifiers and 3 upwards for classification group clubs. | high | opus |  |
| 0x901c60 | 4 | `TurSecondB::record_season_honours` | thiscall(TurSecondB* this) ret 0, tail jump | Forwards the season honours to the promotion group stage. | high | opus |  |
