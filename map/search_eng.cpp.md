# search_eng.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x804f00 | 55 (+1 unwind) | `SearchEngine::SearchEngine` | thiscall(SearchEngine* this) ret 0, returns this | Constructs the find screen search engine, allocating a result array of one pointer per staff record and setting the count to zero. | high | opus |  |
| 0x804fd0 | 7 | `SearchEngine::~SearchEngine` | thiscall(SearchEngine* this) ret 0 | Destroys the search engine by freeing its result array when one is allocated. | high | opus |  |
| 0x804fe0 | 287 | `SearchEngine::find_clubs` | thiscall(SearchEngine* this, const char* text, int national_teams) ret 8 | Fills the result array with clubs or national teams whose names, nation, division or continent text match the search text, then sorts them. | high | opus |  |
| 0x805310 | 1125 | `SearchEngine::find_staff` | thiscall(SearchEngine* this, const char* text, int non_players) ret 8 | Fills the result array with players or non-players that match the search text, or a special keyword such as No Club, Retired or awol. | high | opus |  |
| 0x805f10 | 66 | `search_text_matches_continent` | cdecl(Continent* continent, const char* text) ret 0 | Reports whether the search text occurs in any of the five name fields of a continent record. | medium | opus |  |
| 0x805fb0 | 56 | `search_text_matches_nation` | cdecl(Nation* nation, const char* text) ret 0 | Reports whether the search text occurs in any of the four name fields of a nation record. | medium | opus |  |
| 0x806030 | 36 | `search_text_matches_club` | cdecl(Club* club, const char* text) ret 0 | Reports whether the search text occurs in the long or short name of a club record. | medium | opus |  |
| 0x806080 | 124 | `search_text_matches_staff_name` | cdecl(Staff* staff, const char* text) ret 0 | Formats the staff member's name in each of seven styles and reports whether the search text occurs in any of them. | high | opus |  |
| 0x8061f0 | 46 | `search_text_matches_division` | cdecl(ClubComp* division, const char* text) ret 0 | Reports whether the search text occurs in any of the three name fields of a club competition record. | medium | opus |  |
| 0x806260 | 166 | `search_text_contains` | cdecl(const char* field, char* text, int split_words) ret 0 | Reports whether the text occurs anywhere in a field, or with the split flag whether any space-separated word of it occurs there. | high | opus |  |
