# eng_fa_cup.cpp: 3 globals owned by eng_fa_cup.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969b28 | 160 | vtable | `g_vtable_eng_fa_cup` | Vtable of EngFaCup, 40 slots. | the destructor or constructor of EngFaCup holds it: 0x56f040 EngFaCup::EngFaCup, 0x56f250 EngFaCup::~EngFaCup | high | script |  | [0x56f040](../map/eng_fa_cup.cpp.md), [0x56f250](../map/eng_fa_cup.cpp.md) |  |
| 0xb63dfc | 4 | s32 | `g_league_world_club_comp_count` | g_league_table+0x9c comp_count: number of competition objects in the comp_list of the world club entry. | EngFaCup::collect_entrants loops over the list up to this count. 0x669290 key_nation_delete_all_comps (high) uses the same field of every entry as the list length. | high | sonnet |  | [0x56fab0](../map/eng_fa_cup.cpp.md) |  |
| 0xb63e00 | 4 | void ** | `g_league_world_club_comp_list` | g_league_table+0xa0 comp_list: pointer to the array of competition object pointers that the setup function of the world club entry creates. | 0x56fab0 EngFaCup::collect_entrants reads it to find g_key_club_comp_fifa_club_world_championship (high) among the comps. 0x669290 key_nation_delete_all_comps (high) frees the list of every entry. | high | sonnet |  | [0x56fab0](../map/eng_fa_cup.cpp.md) |  |
