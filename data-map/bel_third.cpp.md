# bel_third.cpp: 1 globals owned by bel_third.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x967b48 | 180 | vtable | `g_vtable_bel_third` | Vtable of BelThird, 45 slots. | the destructor or constructor of BelThird holds it: 0x4216f0 BelThird::BelThird, 0x421940 BelThird::~BelThird | high | script |  | [0x4216f0](../map/bel_third.cpp.md), [0x421940](../map/bel_third.cpp.md) |  |
