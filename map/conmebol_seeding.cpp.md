# conmebol_seeding.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4c5fe0 | 139 | `ConmebolSeeding::ConmebolSeeding` | thiscall(ConmebolSeeding* this), returns this, ret 0 | Waits for the CM01/02 CD, loads the seeding temporary file, or else builds the list of up to eleven CONMEBOL nations with their club places. | medium | opus | 2026-10-14-game-creation-inventory.md, 2026-10-16-sweep-europe.md |
| 0x4c61b0 | 55 | `ConmebolSeeding::update_for_new_season` | thiscall(ConmebolSeeding* this, int skip_flag), ret 4 | Once a new season year starts, stores the year at +0x6f, collects South American clubs and assigns their Libertadores places. | medium | opus |  |
| 0x4c6280 | 132 | `collect_conmebol_clubs` | stdcall-shaped, callee pops 4: (SeedClub **out_array) returns short club count, ret 4 | Builds and sorts a 12-byte record array of South American clubs with nation id, reputation band, division and league position. | medium | opus |  |
| 0x4c6430 | 218 | `ConmebolSeeding::assign_libertadores_places` | thiscall(ConmebolSeeding* this, SeedClub* clubs, short club_count), ret 8 | Marks the Libertadores holder, then fills each of eleven nation quotas with fixed or cup qualifiers and the best remaining clubs. | medium | opus | 2026-10-16-sweep-europe.md |
| 0x4c6730 | 131 | `ConmebolSeeding::find_nth_unqualified_club_of_nation` | thiscall(ConmebolSeeding* this, SeedClub* clubs, short count, int nation_id, char nth, int skip_qualified, int skip_human), returns Club*, ret 0x18, this unused | Binary searches the sorted club records for a nation and returns its nth club not yet qualified and, optionally, not human managed. | medium | opus |  |
| 0x4c6890 | 50 | `ConmebolSeeding::is_mercosur_invited_club` | thiscall(ConmebolSeeding* this, Club* club), returns int bool, ret 4, this unused | Returns 1 when the club id matches one of twenty fixed club ids invited to the Copa Mercosur, otherwise 0. | medium | opus | 2026-10-16-sweep-europe.md |
| 0x4c6960 | 4 | `ConmebolSeeding::set_bra_champ_cup_winner` | thiscall(ConmebolSeeding* this, Club* winner), ret 4 | Stores the club id of the Brazilian champions cup winner at +0x71 so that the club receives a Libertadores place. | medium | opus |  |
| 0x4c6970 | 168 | `ConmebolSeeding::load_from_temp_file` | thiscall(CONMEBOL_SEEDING *this) via ECX, no stack arguments, returns int success, ret 0 | Reads the nation quota count, quota records, season year and cup winner from conmebol_seeding.tmp, resolving nation pointers. | high | opus |  |
| 0x4c6b70 | 154 | `ConmebolSeeding::save_to_temp_file` | thiscall(CONMEBOL_SEEDING *this) via ECX, no stack arguments, ret 0 | Writes the nation quota count, quota records, season year and cup winner club to conmebol_seeding.tmp in the temp folder. | high | opus |  |
