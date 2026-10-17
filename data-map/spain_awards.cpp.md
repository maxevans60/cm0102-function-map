# spain_awards.cpp: 1 globals owned by spain_awards.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96fdd8 | 72 | vtable | `g_vtable_spain_awards` | Vtable of SpainAwards, 18 slots. | the destructor or constructor of SpainAwards holds it: 0x858ea0 SpainAwards::SpainAwards | high | script |  | [0x858ea0](../map/spain_awards.cpp.md) |  |
