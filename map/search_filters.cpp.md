# search_filters.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x806450 | 38 | `SearchFilters::set_defaults` | thiscall(SearchFilters* this) ret 0 | Writes the default value of every search filter, including both flag masks and both attribute range tables. | medium | opus |  |
| 0x8064d0 | 79 | `SearchFilters::reset_general_filters` | thiscall(SearchFilters* this) ret 0 | Resets the general search filter options to their defaults and leaves the attribute range tables unchanged. | medium | opus |  |
| 0x8065d0 | 32 | `SearchFilters::reset_attribute_filters` | thiscall(SearchFilters* this) ret 0 | Resets both attribute range tables of the search filter to their defaults and clears their two option bits. | medium | opus |  |
| 0x806630 | 711 | `SearchFilters::set_option_flag` | thiscall(SearchFilters* this, uint flag_lo, uint flag_hi) returns int changed, ret 8 | Sets one 64-bit search option flag, clears its group siblings, fills the human manager's nation or region and returns whether the mask changed. | high | opus |  |
| 0x806ff0 | 40 | `SearchFilters::set_nationality_nation` | thiscall(SearchFilters* this, int nation_id) returns int, ret 4 | Stores the nationality nation id of the search filter when it lies from -1 to the nation count less one, otherwise shows an assert error. | high | opus |  |
| 0x807090 | 38 | `SearchFilters::set_nationality_region` | thiscall(SearchFilters* this, char region) returns int, ret 4 | Stores the nationality region of the search filter when it lies from 1 to 14, otherwise shows an assert error. | high | opus |  |
| 0x807130 | 38 | `SearchFilters::set_language_option` | thiscall(SearchFilters* this, char option) returns int, ret 4 | Stores the language filter option of the search, from 1 to 3, otherwise shows an assert error. | medium | opus |  |
| 0x8071d0 | 40 | `SearchFilters::set_based_nation` | thiscall(SearchFilters* this, int nation_id) returns int, ret 4 | Stores the nation where the player is based when it lies from -1 to the nation count less one, otherwise shows an assert error. | high | opus |  |
| 0x807270 | 38 | `SearchFilters::set_based_region` | thiscall(SearchFilters* this, char region) returns int, ret 4 | Stores the region where the player is based for the search filter when it lies from 1 to 14, otherwise shows an assert error. | high | opus |  |
| 0x807310 | 38 | `SearchFilters::set_value_band` | thiscall(SearchFilters* this, char band) returns int, ret 4 | Stores the player value band of the search filter, from -1 to 7, otherwise shows an assert error. | medium | opus |  |
| 0x8073b0 | 38 | `SearchFilters::set_job_filter` | thiscall(SearchFilters* this, char job_option) returns int, ret 4 | Stores the staff job option of the search filter, from 1 to 9, otherwise shows an assert error. | medium | opus |  |
| 0x807450 | 1095 (+3 unwind) | `SearchFilters::player_matches_filter` | thiscall(SearchFilters* this, SearchResult* candidate) returns int, ret 4 | Tests one player search candidate against every active filter flag, field and attribute range and returns whether the player passes. | high | opus | 2026-10-14-columns-and-colours-inventory.md |
| 0x808000 | 129 | `SearchFilters::player_matches_filter_fragment_808000` | none (false entry inside 0x807450) | Holds the attribute range loops at the end of SearchFilters::player_matches_filter, with no entry of its own. | high | opus |  |
| 0x808080 | 117 | `SearchFilters::player_matches_filter_fragment_808080` | none (false entry inside 0x807450) | Holds part of the player attribute range loop of SearchFilters::player_matches_filter, with no entry of its own. | high | opus |  |
| 0x808190 | 64 | `SearchFilters::get_attribute_minimum` | thiscall(SearchFilters* this, char attribute, int is_non_player_table) returns char, ret 8 | Returns the minimum value set for one attribute in the player or the non-player attribute range table, otherwise shows an assert error. | high | opus |  |
| 0x808280 | 170 | `SearchFilters::set_attribute_minimum` | thiscall(SearchFilters* this, char attribute, char minimum, int is_non_player_table) returns int changed, ret 0xc | Sets the minimum value for one attribute in the player or non-player range table, updates the active range counts and switches the attribute filter flags. | high | opus |  |
