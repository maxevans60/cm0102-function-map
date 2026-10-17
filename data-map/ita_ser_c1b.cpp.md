# ita_ser_c1b.cpp: 1 globals owned by ita_ser_c1b.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96c5e8 | 180 | vtable | `g_vtable_ita_ser_c1b` | Vtable of ItaSerC1b, 45 slots. | the destructor or constructor of ItaSerC1b holds it: 0x64ec20 ItaSerC1b::ItaSerC1b, 0x64ee70 ItaSerC1b::~ItaSerC1b | high | script |  | [0x64ec20](../map/ita_ser_c1b.cpp.md), [0x64ee70](../map/ita_ser_c1b.cpp.md) |  |
