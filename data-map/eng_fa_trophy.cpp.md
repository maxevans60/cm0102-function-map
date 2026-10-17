# eng_fa_trophy.cpp: 1 globals owned by eng_fa_trophy.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969bc8 | 160 | vtable | `g_vtable_eng_fa_trophy` | Vtable of EngFaTrophy, 40 slots. | the destructor or constructor of EngFaTrophy holds it: 0x570c00 EngFaTrophy::EngFaTrophy, 0x570df0 EngFaTrophy::~EngFaTrophy | high | script |  | [0x570c00](../map/eng_fa_trophy.cpp.md), [0x570df0](../map/eng_fa_trophy.cpp.md) |  |
