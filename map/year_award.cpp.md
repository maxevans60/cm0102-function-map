# year_award.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x92fe80 | 73 (+2 unwind) | `YEAR_AWARD::YEAR_AWARD` | thiscall (YEAR_AWARD *this, 6 award record args, u8 b1d, int shortlist_source, u8 b1e, FILE *load_file, int arg12) ret 0x2c | Constructs a yearly award object, loading its saved state or building a new award shortlist from a source. | high | opus |  |
| 0x92ff60 | 11 | `YEAR_AWARD::`scalar deleting destructor'` | thiscall(YEAR_AWARD* this, u8 flags) ret 4 | Runs the year award destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x92ff80 | 29 (+1 unwind) | `YEAR_AWARD::~YEAR_AWARD` | thiscall(YEAR_AWARD* this) ret 0 | Destroys a year award by restoring vtable 0x9713b8, freeing the owned award shortlist at +0x1f and running the AWARD base destructor. | high | opus |  |
| 0x92fff0 | 137 (+1 unwind) | `YEAR_AWARD::load_from_disk` | thiscall(YEAR_AWARD* this, int shortlist_source, FILE* save_file) ret 8, returns 1 or 0 | Reads the first and last history offsets of a year award from the save file and rebuilds its shortlist, reporting a corrupt save on failure. | high | opus |  |
| 0x9301f0 | 76 | `YEAR_AWARD::save_to_disk` | thiscall(YEAR_AWARD* this, FILE* save_file) ret 4 | Writes the first and last history offsets of a year award and its shortlist to the save file, with an error box on failure. | high | opus |  |
| 0x9302f0 | 166 | `YEAR_AWARD::record_winners` | thiscall(YEAR_AWARD* this, YearAwardRecord* record, int post_news) ret 8 | Adds the year award result to the award history, posts the news when asked, and credits the first, second and third placed players. | high | opus |  |
| 0x9304d0 | 7 | `YEAR_AWARD::get_history_list` | thiscall(YEAR_AWARD* this) ret 0, returns LLIST* | Returns the list of past winners of the year award by reading the history records between its first and last offsets. | high | sonnet |  |
| 0x9304f0 | 291 (+1 unwind) | `YEAR_AWARD::post_winner_news` | thiscall(YEAR_AWARD* this, YearAwardRecord* record) ret 4 | Builds a type 0x1b news item for the year award winners and sends it to division, nation, continent or all managers. | high | opus |  |
| 0x930880 | 871 | `YEAR_AWARD::write_news` | thiscall(YEAR_AWARD* this, NewsItem* item, Text* text, int is_body) ret 0xc | Writes the headline or the body of a year award news item, choosing a template by club, position and date range. | high | opus |  |
