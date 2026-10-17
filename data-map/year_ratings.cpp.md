# year_ratings.cpp: 3 globals owned by year_ratings.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96d7bc | 4 | float | `g_f32_1_2` | Read-only float constant 1.2. | the float at this address in .rdata is 1.2, and every access reads it | high | script |  | [0x6fad40](../map/match_pl.cpp.md), [0x866830](../map/staff_contracts.cpp.md), [0x931f90](../map/year_ratings.cpp.md), [0x9320e0](../map/year_ratings.cpp.md), [0x932230](../map/year_ratings.cpp.md) |  |
| 0x9713c8 | 4 | float | `g_f32_0_00625` | Read-only float constant 0.00625. | the float at this address in .rdata is 0.00625, and every access reads it | high | script |  | [0x932230](../map/year_ratings.cpp.md) |  |
| 0x9713cc | 4 | float | `g_f32_0_0002_9713cc` | Read-only float constant 0.0002. | the float at this address in .rdata is 0.0002, and every access reads it | high | script |  | [0x9323b0](../map/year_ratings.cpp.md), [0x932590](../map/year_ratings.cpp.md) |  |
