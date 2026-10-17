# year_award.cpp: 1 globals owned by year_award.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9713b8 | 16 | vtable | `g_vtable_year_award` | Vtable of YEAR_AWARD, 4 slots. | the destructor or constructor of YEAR_AWARD holds it: 0x92fe80 YEAR_AWARD::YEAR_AWARD, 0x92ff80 YEAR_AWARD::~YEAR_AWARD | high | script |  | [0x92fe80](../map/year_award.cpp.md), [0x92ff80](../map/year_award.cpp.md) |  |
