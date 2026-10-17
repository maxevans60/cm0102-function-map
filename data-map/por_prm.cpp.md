# por_prm.cpp: 1 globals owned by por_prm.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96e6f0 | 180 | vtable | `g_vtable_por_prm` | Vtable of PorPrm, 45 slots. | the destructor or constructor of PorPrm holds it: 0x7ce720 PorPrm::PorPrm, 0x7ce950 PorPrm::~PorPrm | high | script |  | [0x7ce720](../map/por_prm.cpp.md), [0x7ce950](../map/por_prm.cpp.md) |  |
