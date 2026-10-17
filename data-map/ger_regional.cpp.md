# ger_regional.cpp: 1 globals owned by ger_regional.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96b250 | 180 | vtable | `g_vtable_ger_regional` | Vtable of GerRegional, 45 slots. | the destructor or constructor of GerRegional holds it: 0x5dcbd0 GerRegional::GerRegional, 0x5dce30 GerRegional::~GerRegional | high | script |  | [0x5dcbd0](../map/ger_regional.cpp.md), [0x5dce30](../map/ger_regional.cpp.md) |  |
