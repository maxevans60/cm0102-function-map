# ita_c1_super.cpp: 1 globals owned by ita_c1_super.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96c1c4 | 160 | vtable | `g_vtable_ita_c1_super` | Vtable of ItaC1Super, 40 slots. | the destructor or constructor of ItaC1Super holds it: 0x63c5e0 ItaC1Super::ItaC1Super, 0x63c7c0 ItaC1Super::~ItaC1Super | high | script |  | [0x63c5e0](../map/ita_c1_super.cpp.md), [0x63c7c0](../map/ita_c1_super.cpp.md) |  |
