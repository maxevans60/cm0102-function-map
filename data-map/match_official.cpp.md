# match_official.cpp: 2 globals owned by match_official.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96d648 | 4 | float | `g_f32_minus_225` | Read-only float constant -225. | the float at this address in .rdata is -225, and every access reads it | high | script |  | [0x6e9630](../map/match_official.cpp.md), [0x6ea4e0](../map/match_official.cpp.md), [0x6eab60](../map/match_official.cpp.md) |  |
| 0x96d64c | 4 | float | `g_f32_45` | Read-only float constant 45. | the float at this address in .rdata is 45, and every access reads it | high | script |  | [0x6e9630](../map/match_official.cpp.md), [0x6ea4e0](../map/match_official.cpp.md), [0x6eab60](../map/match_official.cpp.md) |  |
