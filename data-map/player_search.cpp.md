# player_search.cpp: 4 globals owned by player_search.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96e2a0 | 8 | double | `g_f64_0_9523809523809523` | Read-only double constant 0.9523809523809523. | the double at this address in .rdata is 0.9523809523809523, and every access reads it | high | script |  | [0x7bca90](../map/player_search.cpp.md) |  |
| 0x96e2a8 | 8 | double | `g_f64_430_0` | Read-only double constant 430.0. | the double at this address in .rdata is 430.0, and every access reads it | high | script |  | [0x7bca90](../map/player_search.cpp.md) |  |
| 0x96e2b0 | 8 | double | `g_f64_0_43` | Read-only double constant 0.43. | the double at this address in .rdata is 0.43, and every access reads it | high | script |  | [0x7bca90](../map/player_search.cpp.md) |  |
| 0xb74438 | 2 | object | `g_scout_club_table_list` | The static global list of club report tables that scout lists add to when they watch a club. | 0x7f6730 scout_manager_static_init_list_b74438 constructs it. 0x7b3d50 PLAYER_SEARCH::set_assigned_club and 0x7b17e0 PLAYER_SEARCH::load add a table to the global list and take it in ECX. | medium | sonnet |  | [0x7ae4f0](../map/player_search.cpp.md), [0x7aee80](../map/player_search.cpp.md), [0x7b14a0](../map/player_search.cpp.md), [0x7b17e0](../map/player_search.cpp.md), [0x7b2bf0](../map/player_search.cpp.md), [0x7b3d50](../map/player_search.cpp.md) and 4 more |  |
