# usa_open_cup.cpp: 1 globals owned by usa_open_cup.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x970998 | 212 | vtable | `g_vtable_usa_open_cup` | Vtable of UsaOpenCup, 53 slots. | the destructor or constructor of UsaOpenCup holds it: 0x90aeb0 UsaOpenCup::UsaOpenCup, 0x90b0a0 UsaOpenCup::~UsaOpenCup | high | script |  | [0x90aeb0](../map/usa_open_cup.cpp.md), [0x90b0a0](../map/usa_open_cup.cpp.md) |  |
