# den_first.cpp: 1 globals owned by den_first.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969630 | 360 | vtable | `g_vtable_den_first` | Vtable of DenFirst, 90 slots. | the destructor or constructor of DenFirst holds it: 0x5516f0 DenFirst::DenFirst, 0x551920 DenFirst::~DenFirst | high | script |  | [0x5516f0](../map/den_first.cpp.md), [0x551920](../map/den_first.cpp.md) |  |
