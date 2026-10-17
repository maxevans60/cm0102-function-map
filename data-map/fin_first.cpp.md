# fin_first.cpp: 2 globals owned by fin_first.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a400 | 180 | vtable | `g_vtable_fin_first` | Vtable of FinFirst, 45 slots. | the destructor or constructor of FinFirst holds it: 0x592eb0 FinFirst::FinFirst, 0x593100 FinFirst::~FinFirst | high | script |  | [0x592eb0](../map/fin_first.cpp.md), [0x593100](../map/fin_first.cpp.md) |  |
| 0x96a4b8 | 8 | double | `g_f64_61_08` | Read-only double constant 61.08. | the double at this address in .rdata is 61.08, and every access reads it | high | script |  | [0x594080](../map/fin_first.cpp.md) |  |
