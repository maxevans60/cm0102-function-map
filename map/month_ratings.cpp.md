# month_ratings.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x767af0 | 17 | `MONTH_RATINGS::MONTH_RATINGS` | thiscall(MONTH_RATINGS* this, FILE* load_source or 0) ret 4, returns this | Constructs an empty month ratings table with month -1 and year 0, and loads it from the save file when a source is given. | high | opus |  |
| 0x767b20 | 176 | `MONTH_RATINGS::load_from_disk` | thiscall(MONTH_RATINGS* this, FILE* save_file) ret 4, returns 1 or 0 | Reads the player count, the 12-byte player entries, the current month and the current year from the save file, reporting corruption or allocation failure. | high | opus |  |
| 0x767d60 | 120 | `MONTH_RATINGS::save_to_disk` | thiscall(MONTH_RATINGS* this, FILE* save_file) ret 4 | Writes the player count, the player entries, the current month and the current year to the save file, with an error box on failure. | high | opus |  |
| 0x767ee0 | 45 | `MONTH_RATINGS::record_match_ratings` | thiscall(MONTH_RATINGS* this, Fixture* fixture, MatchData* match) ret 8 | Adds the rating of every player who took part in a match to the month ratings, for both teams. | medium | opus |  |
| 0x767f60 | 17 | `MONTH_RATINGS::reset` | thiscall(MONTH_RATINGS* this, char month, short year) ret 8 | Frees the month ratings entries, sets the count and capacity to zero and stores the new month and year. | high | opus |  |
| 0x767fa0 | 132 | `MONTH_RATINGS::add_player_rating` | thiscall(MONTH_RATINGS* this, PlayerMatchEntry* entry) ret 4 | Finds or appends the player's 12-byte entry, growing the table by 300, then adds the match rating and counts one more match. | high | opus |  |
| 0x768130 | 75 | `MONTH_RATINGS::find_best_player` | thiscall(MONTH_RATINGS* this, int nation_id or -1, char max_age or -1) ret 8, returns entry pointer or 0 | Sorts the month ratings by average and returns the best entry that matches the nation and age filters, lowering the minimum match count stepwise. | medium | opus |  |
| 0x768200 | 52 | `month_ratings_compare_average` | cdecl(const void* a, const void* b) ret 0, returns -1, 0 or 1 | Orders two month rating entries by average rating, highest first, and puts entries with fewer than three matches last, as a qsort comparator. | high | opus |  |
