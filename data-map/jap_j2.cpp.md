# jap_j2.cpp: 1 globals owned by jap_j2.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96caf4 | 572 | vtable | `g_vtable_jap_j2` | Vtable of JapJ2, 143 slots. | the destructor or constructor of JapJ2 holds it: 0x6644c0 JapJ2::JapJ2, 0x6646f0 JapJ2::~JapJ2 | high | script |  | [0x6644c0](../map/jap_j2.cpp.md), [0x6646f0](../map/jap_j2.cpp.md) |  |
