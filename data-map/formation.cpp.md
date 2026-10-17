# formation.cpp: 2 globals owned by formation.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x98ec54 | 4 | unknown | `g_formation_file_identifier_lowest` | The lowest value that Formation::load_from_disk accepts as the identifier of a formation file. The code uses this address as a number. | 0x5b5d10 Formation::load_from_disk compares the first dword of the file with 0x98ec54 to 0x98ec5e and rejects values below 0x98ec59 as an early version formation. The global itself holds four zero bytes. | medium | sonnet |  | [0x5b5d10](../map/formation.cpp.md) | 2026-10-16-tactics-inventory.md |
| 0x9cc368 | 64 | table | `g_formation_position_code_list` | List of 31 formation position codes as 16 bit values, ended by 0xffff, that Formation::set_slot_coordinate tries when it snaps a slot. | 0x5b3560 Formation::set_slot_coordinate loops over it and passes each code to 0x5b7e60 formation_get_default_coordinate. 0x89f710 tactics_screen_handle_event uses the same loop. | medium | sonnet |  | [0x5b3560](../map/formation.cpp.md), [0x89f710](../map/tactics_screens.cpp.md) | 2026-10-16-tactics-inventory.md |
