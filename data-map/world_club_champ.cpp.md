# world_club_champ.cpp: 2 globals owned by world_club_champ.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x97119c | 180 | vtable | `g_vtable_world_club_champ` | Vtable of WorldClubChamp, 45 slots. | the destructor or constructor of WorldClubChamp holds it: 0x929140 WorldClubChamp::WorldClubChamp, 0x9292d0 WorldClubChamp::~WorldClubChamp | high | script |  | [0x929140](../map/world_club_champ.cpp.md), [0x9292d0](../map/world_club_champ.cpp.md) | 2026-10-16-sweep-europe.md |
| 0xb6473c | 4 | unknown | `g_key_nation_continent_loop_end` | The end address of the continent field loop over the key nation league entries. It is a loop bound, not a stored value. | 0x92ae60 WorldClubChamp::pick_entrant compares a pointer that steps 0x48 bytes from the continent field of the first entry against this address. The 35 entries end here. | medium | sonnet |  | [0x92ae60](../map/world_club_champ.cpp.md) |  |
