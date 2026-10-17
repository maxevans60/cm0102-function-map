# bra_nat_third.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x42d2c0 | 179 (+2 unwind) | `BraNatThird::BraNatThird` | thiscall(BraNatThird* this, short year, Comp* comp_record) ret 8 | Constructs the Brazilian third division on League, then loads saved data or sets up rules, a 56-club pool, fixtures, stats and seven extra group stages. | high | opus |  |
| 0x42d520 | 11 | `BraNatThird::`scalar deleting destructor'` | thiscall(BraNatThird* this, unsigned flags) ret 4 | Destroys the Brazilian third division object and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x42d540 | 67 (+1 unwind) | `BraNatThird::~BraNatThird` | thiscall(BraNatThird* this) ret 0 | Destroys the Brazilian third division, freeing its club pool, table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x42d620 | 640 | `BraNatThird::create_schedule` | thiscall(BraNatThird* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10 | Builds the schedule of a stage, with 14 rounds for the first groups, six rounds for the third-round groups and cup rounds otherwise. | high | opus |  |
| 0x42dc90 | 134 | `BraNatThird::create_table` | thiscall(BraNatThird* this) ret 0, returns int success | Collects up to 56 clubs of this competition into a shuffled pool at +0xee and fills the seven-row table with the first seven of them. | high | opus |  |
| 0x42de50 | 39 | `BraNatThird::set_up_rules` | thiscall(BraNatThird* this) ret 0, returns int | Sets the league rules of the Brazilian third division, with seven-club groups, and builds the schedule for stage -1. | high | opus |  |
| 0x42def0 | 172 | `BraNatThird::start_new_season` | thiscall(BraNatThird* this) ret 0 | Clears the old season and stages, then rebuilds rules, club pool, table, fixtures and the seven group stages for the new year. | high | opus |  |
| 0x42e100 | 177 | `BraNatThird::set_club_progress` | thiscall(BraNatThird* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Maps the three progress codes of a club to display codes for the group, cup and final stages and stores them in its Comp_Stats entry. | high | opus |  |
| 0x42e380 | 50 | `BraNatThird::advance_stage` | thiscall(BraNatThird* this) ret 0 | Moves the competition to its next stage and creates the second-round cup, the two quarter-final groups or the final as the stage counter requires. | high | opus |  |
| 0x42e430 | 211 (+1 unwind) | `BraNatThird::create_second_round_stage` | thiscall(BraNatThird* this) ret 0 | Takes the top two clubs of all eight groups, seeds the sixteen by points and creates the second-round Cup_Stage as stage 7. | high | opus |  |
| 0x42e700 | 213 (+2 unwind) | `BraNatThird::create_third_round_groups` | thiscall(BraNatThird* this) ret 0 | Collects the eight winners of the second-round cup, shuffles them and creates two four-club League_Stage groups as stages 8 and 9. | high | opus |  |
| 0x42e980 | 113 (+1 unwind) | `BraNatThird::create_final_stage` | thiscall(BraNatThird* this) ret 0 | Takes the winners of the two third-round groups and creates the two-club final Cup_Stage as stage 10. | high | opus |  |
| 0x42eb00 | 121 | `BraNatThird::update_staff_records_for_status` | thiscall(BraNatThird* this, Club* club, char status, char stage, ...) ret 0x18 | Adds staff records for group qualification, second-round wins, third-round group exits and the title of the Brazilian third division. | high | opus |  |
| 0x42ec60 | 198 | `BraNatThird::build_fate_news_text` | thiscall(BraNatThird* this, int club_index, char fate, char stage, ..., int full_sentence, ...) ret 0x28 | Writes the news that a club qualifies for the second round or wins the competition, else falls back to the base fate text. | high | opus |  |
| 0x42ee80 | 164 (+1 unwind) | `BraNatThird::create_group_stage` | thiscall(BraNatThird* this, char group) ret 4 | Creates the seven-club League_Stage for one extra group from the club pool and stores it in the stage array at that index. | high | opus |  |
| 0x42f0a0 | 167 | `BraNatThird::set_predicted_positions` | thiscall(BraNatThird* this) ret 0 | Sorts the 56-club pool by reputation and stores predicted final positions, with places shared in bands for the knockout rounds and groups. | high | opus |  |
