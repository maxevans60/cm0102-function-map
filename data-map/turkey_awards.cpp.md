# turkey_awards.cpp: 1 globals owned by turkey_awards.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x970748 | 72 | vtable | `g_vtable_turkey_awards` | Vtable of TurkeyAwards, 18 slots. | the destructor or constructor of TurkeyAwards holds it: 0x901c70 TurkeyAwards::TurkeyAwards | high | script |  | [0x901c70](../map/turkey_awards.cpp.md) |  |
