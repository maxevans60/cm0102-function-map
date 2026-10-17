# nor_cup.cpp: 2 globals owned by nor_cup.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96dd80 | 160 | vtable | `g_vtable_nor_cup` | Vtable of NorCup, 40 slots. | the destructor or constructor of NorCup holds it: 0x78f020 NorCup::NorCup, 0x78f210 NorCup::~NorCup | high | script |  | [0x78f020](../map/nor_cup.cpp.md), [0x78f210](../map/nor_cup.cpp.md) |  |
| 0xa6973c | 2 | char[2] | `g_str_2` | The text "2". | the bytes at this address are the text "2", and every access passes its address | high | script |  | [0x78f890](../map/nor_cup.cpp.md) |  |
