# team_award.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8af520 | 82 (+4 unwind) | `TEAM_AWARD::TEAM_AWARD` | thiscall (TEAM_AWARD *this, 6 award record args, u8 b25, u8 b25c, FILE *load_file, int arg11) ret 0x28 | Constructs a team award object, clears its 20 winner slots and loads saved state when a file is given. | high | opus |  |
| 0x8af630 | 11 | `TEAM_AWARD::`scalar deleting destructor'` | thiscall(TEAM_AWARD* this, u8 flags) ret 4 | Runs the team award destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x8af650 | 2 | `TEAM_AWARD::~TEAM_AWARD` | thiscall(TEAM_AWARD* this) ret 0, tail call | Destroys a team award by restoring vtable 0x9703f0 and running the AWARD base destructor. | high | opus |  |
| 0x8af660 | 157 | `TEAM_AWARD::load_from_disk` | thiscall(TEAM_AWARD* this, FILE* load_file) ret 4, returns 1 or 0 | Reads the update date, the selected team block, the substitute count and both history offsets from the saved game. | high | opus |  |
| 0x8af870 | 138 | `TEAM_AWARD::save_to_disk` | thiscall(TEAM_AWARD* this, FILE* save_file) ret 4 | Writes the update date, the selected team block, the substitute count and both history offsets to the saved game. | high | opus |  |
| 0x8afa40 | 288 | `TEAM_AWARD::add_candidate` | thiscall(TEAM_AWARD* this, Staff* player, Club* club, float rating, u16 position_mask or 0) ret 0x10, returns true when the team is full | Places a player in a free team slot that fits his positions, raising his rating if already chosen, and reports when all slots are filled. | high | opus |  |
| 0x8afd90 | 16 | `TEAM_AWARD::clear_selection` | thiscall(TEAM_AWARD* this) ret 0 | Empties the twenty team slots and resets the count of filled slots to zero. | high | opus |  |
| 0x8afdc0 | 69 | `TEAM_AWARD::init_slot_positions` | thiscall(TEAM_AWARD* this) ret 0 | Sets the position mask of each starting and substitute slot from the formation mode byte of the award. | high | opus |  |
| 0x8aff00 | 24 | `TEAM_AWARD::set_dates` | thiscall(TEAM_AWARD* this, Date* start, Date* end, Date* update) ret 0xc | Copies the period start, the period end and the update date into the team award. | high | opus |  |
| 0x8aff50 | 30 | `TEAM_AWARD::set_season_dates` | thiscall(TEAM_AWARD* this, short year) ret 4 | Sets the award period to run from the year less the season span byte to the given year. | high | opus |  |
| 0x8affb0 | 84 | `TEAM_AWARD::record_winners` | thiscall(TEAM_AWARD* this) ret 0 | Saves the chosen team to the award history, credits each starting player, sends club news and clears the selection. | high | opus |  |
| 0x8b00a0 | 48 (+1 unwind) | `TEAM_AWARD::get_history_list` | thiscall(TEAM_AWARD* this) ret 0, returns LLIST* or 0 | Returns the list of past teams for this award and adds the current team to it when the selection is complete. | high | opus |  |
| 0x8b0140 | 175 (+1 unwind) | `TEAM_AWARD::send_club_news` | thiscall(TEAM_AWARD* this) ret 0 | Sends each human club a type 0x1b news item that names up to three of its players chosen in the team. | high | opus |  |
| 0x8b0370 | 297 | `TEAM_AWARD::write_news` | thiscall(TEAM_AWARD* this, NewsItem* item, int unused, int full_text) ret 0xc | Writes the team award news text that names one, two or three players or counts a club's players, with player and club links. | high | opus |  |
| 0x8b0730 | 226 | `TEAM_AWARD::apply_formation` | thiscall(TEAM_AWARD* this, Formation* formation) ret 4 | Sets the eleven formation slots to the position codes of the award's formation mode for the team drawing. | high | opus |  |
