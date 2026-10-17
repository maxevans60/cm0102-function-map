# usa_mls_all_stars.cpp: 1 globals owned by usa_mls_all_stars.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9708f8 | 160 | vtable | `g_vtable_usa_mls_all_stars` | Vtable of UsaMlsAllStars, 40 slots. | the destructor or constructor of UsaMlsAllStars holds it: 0x90a150 UsaMlsAllStars::UsaMlsAllStars, 0x90a330 UsaMlsAllStars::~UsaMlsAllStars | high | script |  | [0x90a150](../map/usa_mls_all_stars.cpp.md), [0x90a330](../map/usa_mls_all_stars.cpp.md) |  |
