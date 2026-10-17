# Cup.cpp: 3 globals owned by Cup.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9693c8 | 160 | vtable | `g_vtable_cup` | Vtable of Cup, 40 slots. | the destructor or constructor of Cup holds it: 0x518640 Cup::Cup, 0x518690 Cup::~Cup | high | script |  | [0x518640](../map/Cup.cpp.md), [0x518690](../map/Cup.cpp.md) | 2026-10-16-research-name-check.md, 2026-10-16-sweep-europe.md |
| 0xae1880 | 4 | s32 | `g_cup_possible_team_count` | The count of teams that Cup::get_fixture_side_teams found for one side of a fixture. | 0x521790 Cup::get_fixture_side_teams sets it to 0 or 1 and passes its address as the count of 0x5219b0 Cup::collect_possible_teams. | medium | sonnet | [0x521790](../map/Cup.cpp.md) | [0x521790](../map/Cup.cpp.md) |  |
| 0xb63d7e | 4 | ClubComp * | `g_league_world_cup_cup_comp` | g_league_table+0x1e club comp: pointer to the main cup competition record of the world cup entry, null for this entry. | Read by 0x519890 Cup::update_staff_records_for_status, which compares it with the comp of a Cup, and by 0x904580 UefaSeeding::assign_uefa_cup_places. repo doc 2026-10-14-start-new-game-inventory.md section 3c (league entry layout): club comp pointer at +0x1e. | medium | sonnet |  | [0x519890](../map/Cup.cpp.md), [0x519a90](../map/Cup.cpp.md), [0x904580](../map/uefa_seeding.cpp.md), [0x92ae60](../map/world_club_champ.cpp.md) |  |
