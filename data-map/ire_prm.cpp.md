# ire_prm.cpp: 1 globals owned by ire_prm.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96c014 | 180 | vtable | `g_vtable_ire_prm` | Vtable of IrePrm, 45 slots. | the destructor or constructor of IrePrm holds it: 0x639bb0 IrePrm::IrePrm, 0x639e00 IrePrm::~IrePrm | high | script |  | [0x639bb0](../map/ire_prm.cpp.md), [0x639e00](../map/ire_prm.cpp.md) |  |
