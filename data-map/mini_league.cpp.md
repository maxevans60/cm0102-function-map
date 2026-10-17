# mini_league.cpp: 1 globals owned by mini_league.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96d94c | 216 | vtable | `g_vtable_mini_league` | Vtable of MiniLeague, 54 slots. | the destructor or constructor of MiniLeague holds it: 0x766500 MiniLeague::MiniLeague, 0x766800 MiniLeague::MiniLeague, 0x7668f0 MiniLeague::~MiniLeague | high | script |  | [0x766500](../map/mini_league.cpp.md), [0x766800](../map/mini_league.cpp.md), [0x7668f0](../map/mini_league.cpp.md) |  |
