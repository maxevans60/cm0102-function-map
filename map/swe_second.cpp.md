# swe_second.cpp: 18 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8916f0 | 179 (+2 unwind) | `SweSecond::SweSecond` | thiscall(SweSecond* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Swedish Second Division on League, then loads it or sets up rules, the 12-club North table, stats, fixtures and five section stages. | high | opus |  |
| 0x891980 | 11 | `SweSecond::`scalar deleting destructor'` | thiscall(SweSecond* this, unsigned flags), returns this, ret 4 | Runs the SweSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x8919a0 | 60 (+1 unwind) | `SweSecond::~SweSecond` | thiscall(SweSecond* this), ret 0 | Frees the table, the base schedule, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x891a60 | 708 | `SweSecond::create_schedule` | thiscall(SweSecond* this, char stage, short* round_count, short* name_base, int* flag), returns schedule pointer, ret 0x10 | Builds the 22-round section league dates for stages -1 to 4, and the one-round and two-round play-off templates for stages 5 and 6. | high | opus |  |
| 0x8921b0 | 143 | `SweSecond::create_table` | thiscall(SweSecond* this), returns bool, ret 0 | Allocates the 12-row table and fills it with the Second Division clubs of the North section, marking B teams as barred from promotion. | high | opus |  |
| 0x892380 | 36 | `SweSecond::set_up_rules` | thiscall(SweSecond* this), returns int, ret 0 | Sets the league rules of the Swedish Second Division, with promotion to the First Division, and builds the base league schedule. | high | opus |  |
| 0x892410 | 147 | `SweSecond::start_new_season` | thiscall(SweSecond* this), ret 0 | Archives the season, deletes the old stages and rebuilds the rules, table, fixtures, five section stages and predicted positions for the new season. | high | opus |  |
| 0x8925d0 | 47 | `SweSecond::advance_stage` | thiscall(SweSecond* this), ret 0 | Moves to the next stage and builds the promotion and relegation play-off stages when the stage reaches 5. | high | opus |  |
| 0x892670 | 274 (+1 unwind) | `SweSecond::create_section_stage` | thiscall(SweSecond* this, char stage), ret 4 | Builds the League_Stage of one of five regional Second Division sections from the clubs assigned to that section. | high | opus |  |
| 0x892a10 | 136 (+1 unwind) | `SweSecond::create_promotion_play_off_stage` | thiscall(SweSecond* this), ret 0 | Builds stage 5, a Cup_Stage between the six section winners, and draws its round. | high | opus |  |
| 0x892bb0 | 243 (+1 unwind) | `SweSecond::create_relegation_play_off_stage` | thiscall(SweSecond* this), ret 0 | Picks the top 24 Swedish Lower Division clubs, stores twelve for promotion and builds stage 6 against the six section runners-up. | medium | opus |  |
| 0x892ee0 | 195 | `SweSecond::update_staff_records_for_status` | thiscall(SweSecond* this, Club* club, char status, char stage, int, Fixture*, int), returns int, ret 0x18 | Adds staff records for section winners, and sets table status after the promotion and relegation play-offs with promotion or relegation records. | high | opus |  |
| 0x893160 | 159 | `SweSecond::build_fate_news_text` | stdcall(int club_index, char fate, char stage, ..., int full_result, ...), ret 0x28 | Writes news that a club wins or misses promotion in the stage 5 play-off, or avoids relegation or goes down in stage 6. | high | opus |  |
| 0x893320 | 95 | `SweSecond::get_club_array` | thiscall(SweSecond* this, Club*** out_clubs, short* out_count), ret 8 | Allocates an array of the 72 club pointers from the main table and the five section stages and returns it with the count. | high | opus |  |
| 0x893470 | 123 | `SweSecond::set_predicted_positions` | thiscall(SweSecond* this), ret 0 | Sorts the clubs of each of the six sections by strength and stores each rank as the club's predicted position in Comp_Stats. | high | opus |  |
| 0x8935e0 | 90 | `SweSecond::set_club_progress` | stdcall(Club* club, char stage, char code1, char code2, char code3), ret 0x14 | Writes a club's three progress codes in its Comp_Stats entry, scaling section codes and mapping stage 6 play-off codes to 55, 61 and 67. | high | opus |  |
| 0x8936e0 | 10 | `SweSecond::load_extra_data` | thiscall(SweSecond* this, FILE* file), returns 1, ret 4 | Reads the twelve stored promoted club ids at +0xee from the save file. | high | opus |  |
| 0x893700 | 9 | `SweSecond::save_extra_data` | thiscall(SweSecond* this, FILE* file), ret 4 | Writes the twelve stored promoted club ids at +0xee to the save file. | high | opus |  |
