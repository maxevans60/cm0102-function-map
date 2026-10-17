# player_regen.cpp: 7 globals owned by player_regen.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a688 | 8 | double | `g_f64_0_425` | Read-only double constant 0.425. | the double at this address in .rdata is 0.425, and every access reads it | high | script |  | [0x7abac0](../map/player_regen.cpp.md) |  |
| 0x96d300 | 8 | double | `g_f64_6000_0` | Read-only double constant 6000.0. | the double at this address in .rdata is 6000.0, and every access reads it | high | script |  | [0x6beeb0](../map/match_eng.cpp.md), [0x6df460](../map/match_man.cpp.md), [0x7a59e0](../map/player_regen.cpp.md), [0x7a65d0](../map/player_regen.cpp.md) |  |
| 0x96e288 | 8 | double | `g_f64_4500_0` | Read-only double constant 4500.0. | the double at this address in .rdata is 4500.0, and every access reads it | high | script |  | [0x7a59e0](../map/player_regen.cpp.md), [0x7a65d0](../map/player_regen.cpp.md) |  |
| 0x96e290 | 8 | double | `g_f64_3750_0` | Read-only double constant 3750.0. | the double at this address in .rdata is 3750.0, and every access reads it | high | script |  | [0x7a59e0](../map/player_regen.cpp.md) |  |
| 0x96e298 | 8 | double | `g_f64_5750_0` | Read-only double constant 5750.0. | the double at this address in .rdata is 5750.0, and every access reads it | high | script |  | [0x7a59e0](../map/player_regen.cpp.md) |  |
| 0xb63d7d | 1 | u8 | `g_league_world_cup_retirement_year_flag` | g_league_table+0x1d retirement_year_flag: byte that the player regen retirement checks test to choose the retirement year for the world cup entry. | Read by 0x7a7310 player_regen_check_retirement and 0x7a79c0 player_regen_check_initial_retirement. 0x830620 create_world_cup_qualifying_comps (high) stores 2 here. | medium | sonnet |  | [0x7a7310](../map/player_regen.cpp.md), [0x7a79c0](../map/player_regen.cpp.md) |  |
| 0xb7434a | 1 | u8 | `g_player_setup_preset_tactics_flag` | Flag set when player_setup.cfg has a PRESET_TACTICS line, which tactics_screen_build reads. | 0x7a3140 player_setup_type_from_name (high) returns 0x2000 for the keyword PRESET_TACTICS, and 0x7a3a10 sets this byte for 0x2000. 0x899ea0 tactics_screen_build reads it. | high | sonnet | [0x7a3a10](../map/player_regen.cpp.md) | [0x899ea0](../map/tactics_screens.cpp.md) | 2026-10-16-tactics-inventory.md |
