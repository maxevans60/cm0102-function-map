# ita_ser_c2a.cpp: 1 globals owned by ita_ser_c2a.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96c69c | 180 | vtable | `g_vtable_ita_ser_c2a` | Vtable of ItaSerC2a, 45 slots. | the destructor or constructor of ItaSerC2a holds it: 0x652e90 ItaSerC2a::ItaSerC2a, 0x6530e0 ItaSerC2a::~ItaSerC2a | high | script |  | [0x652e90](../map/ita_ser_c2a.cpp.md), [0x6530e0](../map/ita_ser_c2a.cpp.md) |  |
