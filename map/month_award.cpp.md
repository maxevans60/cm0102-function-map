# month_award.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x766e10 | 84 (+1 unwind) | `MONTH_AWARD::MONTH_AWARD` | thiscall(MONTH_AWARD* this, 6 award base args, char start_month, u16 start_year, char end_month, u16 end_year, FILE* load_source or 0, int arg) ret 0x30 | Constructs a month award on the AWARD base with up to twelve month slots and loads saved state when a source is given. | high | opus |  |
| 0x766f20 | 11 | `MONTH_AWARD::`scalar deleting destructor'` | thiscall(MONTH_AWARD* this, u8 flags) ret 4 | Runs the month award destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x766f40 | 2 | `MONTH_AWARD::~MONTH_AWARD` | thiscall(MONTH_AWARD* this) ret 0, tail jump to AWARD::~AWARD | Destroys a month award by restoring vtable 0x96da00 and passing on to the AWARD base destructor. | high | opus |  |
| 0x766f4e | 2 | `MONTH_AWARD::~MONTH_AWARD_fragment_766f4e` | not a function entry: nop padding between 0x766f4b and 0x766f50 | Forms two nop padding bytes before MONTH_AWARD::load_from_disk and is a false function entry. | high | opus |  |
| 0x766f50 | 83 | `MONTH_AWARD::load_from_disk` | thiscall(MONTH_AWARD* this, FILE* save_file) ret 4, returns 1 or 0 | Reads the month slots and slot count of a month award from the save file and reports a corrupted save on failure. | high | opus |  |
| 0x767070 | 67 | `MONTH_AWARD::save_to_disk` | thiscall(MONTH_AWARD* this, FILE* save_file) ret 4 | Writes the month slots and slot count of a month award to the save file and shows an error box on failure. | high | opus |  |
| 0x767150 | 46 | `MONTH_AWARD::award_best_rated_player` | thiscall(MONTH_AWARD* this, MONTH_RATINGS* ratings, char max_age or -1) ret 8 | Picks the best rated player of the month ratings for the award's nation and records him and his club as the winner for that month. | high | opus |  |
| 0x7671c0 | 105 | `MONTH_AWARD::set_winner` | thiscall(MONTH_AWARD* this, int staff_id, int club_id, char month, short year) ret 0x10 | Stores the winner and club in the slot for the month, raises the winner's reputation, posts the winner news and updates the staff records. | high | opus |  |
| 0x7672e0 | 26 | `MONTH_AWARD::start_new_season` | thiscall(MONTH_AWARD* this, short year) ret 4 | Moves every month slot on by one year and clears its winner and club when the first slot year differs from the given year. | high | opus |  |
| 0x767330 | 189 (+1 unwind) | `MONTH_AWARD::post_winner_news` | thiscall(MONTH_AWARD* this, char slot_index) ret 4 | Builds a type 0x1b news item for the winner of a month slot and sends it to the relevant managers. | high | opus |  |
| 0x767580 | 430 | `MONTH_AWARD::write_news` | thiscall(MONTH_AWARD* this, NewsItem* item, Text* text, int is_body) ret 0xc | Writes the headline or body text of a month award news item, choosing one of several templates by the winner's club and player-boss state. | high | opus |  |
