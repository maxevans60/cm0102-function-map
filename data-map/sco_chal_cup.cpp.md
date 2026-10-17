# sco_chal_cup.cpp: 1 globals owned by sco_chal_cup.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96f374 | 160 | vtable | `g_vtable_sco_chal_cup` | Vtable of ScoChalCup, 40 slots. | the destructor or constructor of ScoChalCup holds it: 0x7ec980 ScoChalCup::ScoChalCup, 0x7ecb70 ScoChalCup::~ScoChalCup | high | script |  | [0x7ec980](../map/sco_chal_cup.cpp.md), [0x7ecb70](../map/sco_chal_cup.cpp.md) |  |
