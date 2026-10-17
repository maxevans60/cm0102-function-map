# cup_stage.cpp: 1 globals owned by cup_stage.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969468 | 160 | vtable | `g_vtable_cup_stage` | Vtable of Cup_Stage, 40 slots. | the destructor or constructor of Cup_Stage holds it: 0x522e00 Cup_Stage::Cup_Stage, 0x5230e0 Cup_Stage::Cup_Stage, 0x523300 Cup_Stage::~Cup_Stage | high | script |  | [0x522e00](../map/cup_stage.cpp.md), [0x5230e0](../map/cup_stage.cpp.md), [0x523300](../map/cup_stage.cpp.md) | 2026-10-16-research-name-check.md |
