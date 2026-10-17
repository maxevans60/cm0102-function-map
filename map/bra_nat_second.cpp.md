# bra_nat_second.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x42be40 | 160 (+2 unwind) | `BraNatSecond::BraNatSecond` | thiscall(BraNatSecond* this, short year, void* comp_record) ret 8 | Constructs the Brazilian second division on League, loads it from the temp file or sets rules, fills the 28-club table, fixtures and predictions. | high | opus |  |
| 0x42c060 | 11 | `BraNatSecond::`scalar deleting destructor'` | thiscall(BraNatSecond* this, unsigned flags) ret 4 | Runs the BraNatSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x42c080 | 60 (+1 unwind) | `BraNatSecond::~BraNatSecond` | thiscall(BraNatSecond* this) ret 0 | Destroys the second division: frees the table, the schedule and every stage object, then the Comp_Stats block and the League base. | high | opus |  |
| 0x42c140 | 995 | `BraNatSecond::create_schedule` | thiscall(BraNatSecond* this, char stage, short* round_count, short* out_count, int* out_flag) ret 0x10 | Builds the 27-round league schedule for stage -1 and the two-round play-off cup schedule with a 500,000 prize for stage 0. | high | opus |  |
| 0x42ca70 | 84 | `BraNatSecond::create_table` | thiscall(BraNatSecond* this) ret 0, returns bool | Allocates the 28-row league table and fills it with the clubs whose division is the national second division. | high | opus |  |
| 0x42cb70 | 43 | `BraNatSecond::set_up_rules` | thiscall(BraNatSecond* this) ret 0, returns 1 | Sets the second division rule bytes, the first division as upper and third division as lower league with two relegation places, then builds the schedule. | high | opus |  |
| 0x42cc10 | 143 | `BraNatSecond::start_new_season` | thiscall(BraNatSecond* this) ret 0 | Starts a new season: frees the old table and stages, archives Comp_Stats, increments the year, then rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x42cdd0 | 40 | `BraNatSecond::advance_stage` | thiscall(BraNatSecond* this) ret 0 | Moves to the next stage and creates the play-off cup stage when the league stage ends, or reports an error past the last stage. | high | opus |  |
| 0x42ce60 | 148 (+1 unwind) | `BraNatSecond::create_play_off_stage` | thiscall(BraNatSecond* this) ret 0 | Takes the top four clubs of the league table, pairs first with fourth and second with third, and creates the play-off Cup_Stage as stage 0. | high | opus |  |
| 0x42d040 | 52 | `BraNatSecond::update_staff_records_for_status` | thiscall(BraNatSecond* this, Club* club, char result, char stage, int a4, int a5, int a6) ret 0x18 | Adds a morale bonus for promotion and a relegation record in the league stage, and the champions record in the play-off stage. | high | opus |  |
| 0x42d0d0 | 148 | `BraNatSecond::build_fate_news_text` | thiscall(BraNatSecond* this, int club_index, char result, char stage, int a5, int a6, int a7, int comp_id, int a9, int has_partner, int a11) ret 0x28 | Writes the news that a club wins the second division or loses its final, and defers other fates to the Comp base. | high | opus |  |
| 0x42d260 | 30 | `BraNatSecond::set_club_progress` | thiscall(BraNatSecond* this, Club* club, char stage, char code_a, char code_b, char code_c) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, replacing low codes with defaults in the league stage. | high | opus |  |
