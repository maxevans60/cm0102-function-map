# eng_third.cpp: 1 globals owned by eng_third.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969e84 | 180 | vtable | `g_vtable_eng_third` | Vtable of EngThird, 45 slots. | the destructor or constructor of EngThird holds it: 0x576dd0 EngThird::EngThird, 0x577020 EngThird::~EngThird | high | script |  | [0x576dd0](../map/eng_third.cpp.md), [0x577020](../map/eng_third.cpp.md) |  |
