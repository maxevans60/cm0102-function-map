# scout_manager.cpp: 2 globals owned by scout_manager.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xb7443a | 4 | u32 | `g_scout_club_table_list_head` | g_scout_club_table_list+0x2 head: the first entry pointer of the list, copied to the cursor before a walk. | 0x7f9720 SCOUT_MANAGER::fixture_has_scouted_player copies it to 0xb74442 and then steps through the entries with the list iterator. | medium | sonnet |  | [0x7f9720](../map/scout_manager.cpp.md) |  |
| 0xb74442 | 4 | u32 | `g_scout_club_table_list_cursor` | g_scout_club_table_list+0xa cursor: the current entry pointer while the list is walked. | Written only by 0x7f9720 SCOUT_MANAGER::fixture_has_scouted_player from 0xb7443a before it walks the list. | medium | sonnet | [0x7f9720](../map/scout_manager.cpp.md) |  |  |
