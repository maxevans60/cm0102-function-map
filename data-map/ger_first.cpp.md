# ger_first.cpp: 4 globals owned by ger_first.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96b0e4 | 180 | vtable | `g_vtable_ger_first` | Vtable of GerFirst, 45 slots. | the destructor or constructor of GerFirst holds it: 0x5d99b0 GerFirst::GerFirst, 0x5d9be0 GerFirst::~GerFirst | high | script |  | [0x5d99b0](../map/ger_first.cpp.md), [0x5d9be0](../map/ger_first.cpp.md) |  |
| 0x96b198 | 8 | double | `g_f64_0_278` | Read-only double constant 0.278. | the double at this address in .rdata is 0.278, and every access reads it | high | script |  | [0x5dbbd0](../map/ger_first.cpp.md) |  |
| 0x96b1a0 | 8 | double | `g_f64_47_55` | Read-only double constant 47.55. | the double at this address in .rdata is 47.55, and every access reads it | high | script |  | [0x5dbbd0](../map/ger_first.cpp.md) |  |
| 0x96b1a8 | 8 | double | `g_f64_54_321` | Read-only double constant 54.321. | the double at this address in .rdata is 54.321, and every access reads it | high | script |  | [0x5dbbd0](../map/ger_first.cpp.md) |  |
