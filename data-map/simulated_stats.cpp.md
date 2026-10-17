# simulated_stats.cpp: 3 globals owned by simulated_stats.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xdd7160 | 1 | u8 | `g_simulated_stats_static_init_flags` | Flag byte whose first bit marks that the static match record array in play_daily_matches is built. | read and written only by 0x84be20 SimulatedStats::play_daily_matches (medium), which ors in bit 1 once | medium | sonnet | [0x84be20](../map/simulated_stats.cpp.md) | [0x84be20](../map/simulated_stats.cpp.md) |  |
| 0xdd7168 | 287 | object | `g_simulated_stats_static_match_record` | Static match record object that play_daily_matches uses, destroyed at exit. | destroyed by 0x84c500 simulated_stats_atexit_static_match_record (high) and passed by address in 0x84be20 | high | sonnet |  | [0x84be20](../map/simulated_stats.cpp.md), [0x84c500](../map/simulated_stats.cpp.md) |  |
| 0xdd7287 | 3146 | buffer | `g_simulated_stats_static_match_records` | Static array of two 0x625 byte objects that play_daily_matches constructs once. | passed by 0x84be20 SimulatedStats::play_daily_matches (medium) to the array constructor with element size 0x625 and count 2 | medium | sonnet |  | [0x84be20](../map/simulated_stats.cpp.md) |  |
