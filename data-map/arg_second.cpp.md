# arg_second.cpp: 1 globals owned by arg_second.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xadae04 | 1 | s8 | `g_average_sort_season_column` | The season column that the relegation average comparator uses to order its rows. | Written with 2 by 0x408630 ArgSecond::create_promotion_cup_stage and 0x408910 ArgSecond::create_promotion_playoffs. Read by 0x48f450 comp_compare_average_rows_by_season, which limits it to 0 to 3. | medium | sonnet | [0x408630](../map/arg_second.cpp.md), [0x408910](../map/arg_second.cpp.md) | [0x48f450](../map/comp.cpp.md) |  |
