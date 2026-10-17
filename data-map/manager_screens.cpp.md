# manager_screens.cpp: 2 globals owned by manager_screens.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xa14f54 | 4 | s32 | `g_manager_stats_nation_id` | The nation id that the Manager Stats screen was built for, or minus one for the world view. | Written from screen parameter 0 by 0x6ae2a0 manager_stats_screen_build. 0x6b36f0 compare_manager_stats_rows compares it with minus one and with nation id fields of the rows. | medium | sonnet | [0x6ae2a0](../map/manager_screens.cpp.md) | [0x6b36f0](../map/manager_screens.cpp.md) |  |
| 0xa14f58 | 1 | u8 | `g_manager_stats_sort_mode` | The view number of the Manager Stats screen, from 1 to 16, that picks the column the rows sort by. | Written from screen parameter 8 by 0x6ae2a0 manager_stats_screen_build. 0x6b36f0 compare_manager_stats_rows branches on 1, 2, 3 and on to pick the compared value. | medium | sonnet | [0x6ae2a0](../map/manager_screens.cpp.md) | [0x6b36f0](../map/manager_screens.cpp.md) |  |
