# uefa_seeding.cpp: 2 globals owned by uefa_seeding.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xb63d7b | 2 | u16 | `g_league_world_cup_first_season_year` | g_league_table+0x1b first_season_year: year of the first season of the world cup entry, which the setup function stores. | The setup function 0x830620 create_world_cup_qualifying_comps (high) stores 1996 here. 0x904580 UefaSeeding::assign_uefa_cup_places compares it with the season year of a comp. | medium | sonnet |  | [0x904580](../map/uefa_seeding.cpp.md) |  |
| 0xb63d82 | 4 | ClubComp * | `g_league_world_cup_second_cup_comp` | g_league_table+0x22 club comp: pointer to the second cup competition record of the world cup entry, null for this entry. | 0x904580 UefaSeeding::assign_uefa_cup_places passes it to comp_util_get_latest_placed_club. repo doc 2026-10-14-start-new-game-inventory.md section 3c (league entry layout): second club comp pointer at +0x22, the English League Cup for England. | medium | sonnet |  | [0x904580](../map/uefa_seeding.cpp.md) |  |
