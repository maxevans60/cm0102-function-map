# african_nations.cpp: 1 globals owned by african_nations.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x967270 | 180 | vtable | `g_vtable_african_nations` | Vtable of AfricanNations, 45 slots. | the destructor or constructor of AfricanNations holds it: 0x401000 AfricanNations::AfricanNations, 0x401220 AfricanNations::~AfricanNations | high | script |  | [0x401000](../map/african_nations.cpp.md), [0x401220](../map/african_nations.cpp.md) | 2026-10-16-sweep-europe.md, 2026-10-16-sweep-international.md |
