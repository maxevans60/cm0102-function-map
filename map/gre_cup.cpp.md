# gre_cup.cpp: 19 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5e88a0 | 175 (+2 unwind) | `GreCup::GreCup` | thiscall(GreCup* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Greek Cup on League, then loads saved data or picks the 44 entrants and builds rules, the first group and ten group stages. | high | opus |  |
| 0x5e8af0 | 11 | `GreCup::`scalar deleting destructor'` | thiscall(GreCup* this, unsigned flags), returns this, ret 4 | Runs the GreCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5e8b10 | 66 (+1 unwind) | `GreCup::~GreCup` | thiscall(GreCup* this), ret 0 | Destroys the Greek Cup, freeing its table, schedule, entrant list, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5e8bf0 | 410 | `GreCup::create_schedule` | thiscall(GreCup* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the six-round group schedule for stages below 10, or the five-round knockout table with draw and match dates for stage 10. | high | opus |  |
| 0x5e9140 | 98 | `GreCup::build_fate_news_text` | thiscall(GreCup* this, int club_index, char fate, char stage, ..., int full_sentence, ...), ret 0x28 | Writes the news text for a club that goes through or out of a Greek Cup group, or wins or loses a knockout tie. | high | opus |  |
| 0x5e9260 | 68 | `GreCup::create_table` | thiscall(GreCup* this), returns 1 on success and 0 on failure, ret 0 | Allocates the four-row table of the cup's own first group, fills it from entrant column 0 and sends the group draw news. | high | opus |  |
| 0x5e9350 | 38 | `GreCup::set_up_rules` | thiscall(GreCup* this), returns 1, ret 0 | Sets the Greek Cup group rule bytes, with no leagues above or below and a 600000 prize fund, and builds the group schedule. | high | opus |  |
| 0x5e93e0 | 4 | `GreCup::record_season_honours` | thiscall(GreCup* this), ret 0 | Passes the season honours call to the knockout stage object, stage 10, so that it records the cup winners. | high | opus |  |
| 0x5e93f0 | 151 | `GreCup::start_new_season` | thiscall(GreCup* this), ret 0 | Clears the old season and stages, moves the year on, picks new entrants and rebuilds rules, the first group and the ten group stages. | high | opus |  |
| 0x5e95c0 | 40 | `GreCup::advance_stage` | thiscall(GreCup* this), ret 0 | Moves the current stage index on by one and creates the knockout stage when it reaches stage 10. | high | opus |  |
| 0x5e9650 | 155 (+1 unwind) | `GreCup::create_group_stage` | thiscall(GreCup* this, int stage), returns 1 on success and 0 on failure, ret 4 | Creates a four-club League_Stage for one Greek Cup group from entrant column stage plus one, stores it and sends the group draw news. | high | opus |  |
| 0x5e9850 | 181 (+1 unwind) | `GreCup::create_knockout_stage` | thiscall(GreCup* this), ret 0 | Collects the 11 group runners-up and the 11 shuffled group winners into a 22-club Cup_Stage as stage 10 and draws its first round. | high | opus |  |
| 0x5e9a80 | 160 | `GreCup::collect_entrants` | thiscall(GreCup* this), returns 1 on success and 0 on failure, ret 0 | Builds the 44-club entrant list from 16 sorted lower division clubs, then all second division and premier division clubs. | high | opus |  |
| 0x5e9ca0 | 122 | `GreCup::update_staff_records_for_status` | thiscall(GreCup* this, Club* club, char status, char stage, int, Fixture* match, int), returns 0, ret 0x18 | Adds the staff record for a club that leaves a group, goes out of or passes a knockout round, wins the cup or finishes runner-up. | high | opus |  |
| 0x5e9df0 | 141 | `GreCup::load_extra_data` | thiscall(GreCup* this, FILE* file), returns 1 on success and 0 on failure, ret 4 | Reads the entrant count and the entrant club ids from the save file and turns each id back into a club pointer. | high | opus |  |
| 0x5e9fb0 | 65 | `GreCup::save_extra_data` | thiscall(GreCup* this, FILE* file), ret 4 | Writes the entrant count and the entrant club ids to the save file, then restores the club pointers. | high | opus |  |
| 0x5ea060 | 203 | `GreCup::set_predicted_positions` | thiscall(GreCup* this), ret 0 | Sorts a copy of the entrants by reputation and gives each club a predicted final position by knockout round sizes, then in blocks of eleven. | high | opus |  |
| 0x5ea2d0 | 65 | `GreCup::set_club_progress` | thiscall(GreCup* this, Club* club, char stage, char code1, char code2, char code3), ret 0x14 | Maps group stage progress codes to final position codes and writes the three progress bytes of a club's Comp_Stats entry. | high | opus |  |
| 0x5ea3d0 | 13 | `GreCup::set_fixture_substitutes` | thiscall(GreCup* this, Fixture* fixture), ret 4 | Sets the substitutes byte of a Greek Cup fixture to 0x77 when the fixture stage is 10, else to 0x37. | high | opus |  |
