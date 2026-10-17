# fifa_confed.cpp: 1 globals owned by fifa_confed.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a270 | 180 | vtable | `g_vtable_fifa_confed` | Vtable of FifaConfed, 45 slots. | the destructor or constructor of FifaConfed holds it: 0x58b310 FifaConfed::FifaConfed, 0x58b4a0 FifaConfed::~FifaConfed | high | script |  | [0x58b310](../map/fifa_confed.cpp.md), [0x58b4a0](../map/fifa_confed.cpp.md) | 2026-10-16-sweep-international.md |
