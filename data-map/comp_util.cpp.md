# comp_util.cpp: 3 globals owned by comp_util.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x968a88 | 8 | double | `g_f64_0_12004801920768307` | Read-only double constant 0.12004801920768307. | the double at this address in .rdata is 0.12004801920768307, and every access reads it | high | script |  | [0x4b02e0](../map/comp_util.cpp.md) |  |
| 0xae0ff8 | 4 | Club * | `g_club_honours_club` | The club whose honours the club honours sort is collecting. | Written by 0x4c0140 comp_util_collect_club_honours from its club argument. 0x4c02f0 compare_club_honours compares it with the winner, second place and third place clubs of each row. | high | sonnet | [0x4c0140](../map/comp_util.cpp.md) | [0x4c02f0](../map/comp_util.cpp.md) |  |
| 0xae0ffc | 4 | Club * | `g_club_honours_other_club` | The optional second club whose honours the club honours sort also collects. | Written by 0x4c0140 comp_util_collect_club_honours from its second club argument. 0x4c02f0 compare_club_honours tests it when it is not null. | high | sonnet | [0x4c0140](../map/comp_util.cpp.md) | [0x4c02f0](../map/comp_util.cpp.md) |  |
