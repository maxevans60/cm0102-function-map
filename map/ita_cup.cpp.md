# ita_cup.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63e900 | 175 (+2 unwind) | `ItaCup::ItaCup` | thiscall(ItaCup* this, short comp_id, Nation* nation), returns this, ret 8 | Builds the Italian cup on top of League, picks its 48 entrants, then sets up rules, fixtures and the eight first round groups. | high | opus |  |
| 0x63eb50 | 11 | `ItaCup::`scalar deleting destructor'` | thiscall(ItaCup* this, unsigned flags), returns this, ret 4 | Runs the ItaCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x63eb70 | 66 (+1 unwind) | `ItaCup::~ItaCup` | thiscall(ItaCup* this), ret 0 | Destroys the Italian cup by freeing its table, schedule, entrant list, group stages and statistics, then runs the League destructor. | high | opus |  |
| 0x63ec50 | 349 | `ItaCup::create_schedule` | thiscall(ItaCup* this, char stage, short* round_count, short* stage_id, int* is_league), returns schedule pointer, ret 0x10 | Returns the match dates for one stage: three group matchdays for stages 0 to 6, or five knockout rounds for stage 7. | high | opus |  |
| 0x63f130 | 98 | `ItaCup::build_fate_news_text` | thiscall(ItaCup* this, int club_index, char outcome, char stage, ..., int has_result, int extra), ret 0x28 | Writes the news text for a club's group or knockout result, including the through to first round line for a group winner. | high | opus |  |
| 0x63f250 | 71 | `ItaCup::create_first_group_table` | thiscall(ItaCup* this), returns 1 or 0, ret 0 | Sets the group size to four, allocates the cup's own league table, places the first four entrants in it and sends the group draw news. | medium | opus |  |
| 0x63f350 | 37 | `ItaCup::set_up_rules` | thiscall(ItaCup* this), returns 1, ret 0 | Sets the group rules, points and prize values of the Italian cup, then builds the group schedule. | high | opus |  |
| 0x63f3e0 | 151 | `ItaCup::start_new_season` | thiscall(ItaCup* this), ret 0 | Clears last season's tables and stages, increments the season, picks new entrants and rebuilds the eight first round groups. | high | opus |  |
| 0x63f5b0 | 40 | `ItaCup::advance_stage` | thiscall(ItaCup* this), ret 0 | Moves the cup to its next stage and builds the knockout stage when the stage counter reaches seven, asserting if it overruns. | high | opus |  |
| 0x63f640 | 173 (+1 unwind) | `ItaCup::create_group_stage` | thiscall(ItaCup* this, int group_index), returns 1 or 0, ret 4 | Takes the next four entrants from the list, builds a League_Stage group for them and sends the group draw news. | high | opus |  |
| 0x63f870 | 185 (+1 unwind) | `ItaCup::create_knockout_stage` | thiscall(ItaCup* this), ret 0 | Builds the 24-club knockout stage from the eight group winners and the sixteen seeded entrants, then draws its first round. | high | opus |  |
| 0x63faf0 | 327 | `ItaCup::select_entrants` | thiscall(ItaCup* this), returns 1 or 0, ret 0 | Picks the 48 Italian entrants, seeds 32 lower clubs into eight random groups, then adds Serie B leaders and Serie A clubs. | high | opus |  |
| 0x63ff00 | 122 | `ItaCup::update_staff_records_for_status` | thiscall(ItaCup* this, Club* club, char status, char stage, int arg, Fixture* fixture, int arg2), returns 0, ret 0x18 | Adds the staff history record for a club's group qualification, group exit, knockout exit, cup win or runner-up finish. | high | opus |  |
| 0x640050 | 141 | `ItaCup::load_extra_data` | thiscall(ItaCup* this, FILE* file), returns 1 or 0, ret 4 | Reads the entrant count and club index list from a saved game and turns each index into a club pointer. | high | opus |  |
| 0x640210 | 203 | `ItaCup::set_predicted_positions` | thiscall(ItaCup* this), ret 0 | Sorts the entrants by strength and stores a predicted final position for each club in the cup statistics. | high | opus |  |
| 0x640480 | 75 | `ItaCup::set_club_progress` | thiscall(ItaCup* this unused, Club* club, char stage, char progress, char round_a, char round_b), ret 0x14 | Stores a club's progress codes in its cup statistics entry, mapping codes 1 to 4 to round codes when the stage is below 7. | high | opus |  |
| 0x640590 | 136 | `compare_clubs_by_seeding_pot` | cdecl(Club** a, Club** b), returns int, ret 0 | Compares two clubs by Italian cup seeding pot, which it takes from their last division and last league position. | medium | opus |  |
