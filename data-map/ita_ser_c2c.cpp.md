# ita_ser_c2c.cpp: 3 globals owned by ita_ser_c2c.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96c804 | 180 | vtable | `g_vtable_ita_ser_c2c` | Vtable of ItaSerC2c, 45 slots. | the destructor or constructor of ItaSerC2c holds it: 0x65b4e0 ItaSerC2c::ItaSerC2c, 0x65b730 ItaSerC2c::~ItaSerC2c | high | script |  | [0x65b4e0](../map/ita_ser_c2c.cpp.md), [0x65b730](../map/ita_ser_c2c.cpp.md) |  |
| 0x9ea890 | 6 | char[6] | `g_str_nardo` | The text "Nardò". | the bytes at this address are the text "Nardò", and every access passes its address | high | script |  | [0x65c8e0](../map/ita_ser_c2c.cpp.md) |  |
| 0x9ea8bc | 8 | char[8] | `g_str_paterno` | The text "Paternò". | the bytes at this address are the text "Paternò", and every access passes its address | high | script |  | [0x65c8e0](../map/ita_ser_c2c.cpp.md) |  |
