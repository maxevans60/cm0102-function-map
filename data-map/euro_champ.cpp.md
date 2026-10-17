# euro_champ.cpp: 1 globals owned by euro_champ.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a020 | 180 | vtable | `g_vtable_euro_champ` | Vtable of EuroChamp, 45 slots. | the destructor or constructor of EuroChamp holds it: 0x57a890 EuroChamp::EuroChamp, 0x57aad0 EuroChamp::~EuroChamp | high | script |  | [0x57a890](../map/euro_champ.cpp.md), [0x57aad0](../map/euro_champ.cpp.md) | 2026-10-16-sweep-international.md |
