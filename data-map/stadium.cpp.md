# stadium.cpp: 7 globals owned by stadium.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96fe20 | 8 | double | `g_f64_3_25` | Read-only double constant 3.25. | the double at this address in .rdata is 3.25, and every access reads it | high | script |  | [0x85cba0](../map/stadium.cpp.md) |  |
| 0x96fe28 | 8 | double | `g_f64_minus_6_0` | Read-only double constant -6.0. | the double at this address in .rdata is -6.0, and every access reads it | high | script |  | [0x85cba0](../map/stadium.cpp.md) |  |
| 0x96fe30 | 8 | double | `g_f64_8_333333333333333eminus_05` | Read-only double constant 8.333333333333333e-05. | the double at this address in .rdata is 8.333333333333333e-05, and every access reads it | high | script |  | [0x85da00](../map/stadium.cpp.md) |  |
| 0x96fe38 | 8 | double | `g_f64_0_5882352941176471` | Read-only double constant 0.5882352941176471. | the double at this address in .rdata is 0.5882352941176471, and every access reads it | high | script |  | [0x85da00](../map/stadium.cpp.md) |  |
| 0x96fe40 | 8 | double | `g_f64_44_44444444444444` | Read-only double constant 44.44444444444444. | the double at this address in .rdata is 44.44444444444444, and every access reads it | high | script |  | [0x85da00](../map/stadium.cpp.md) |  |
| 0xa835a4 | 4 | s32 | `g_stadium_stashed_venue_id` | The id of a stadium record that Stadium::daily_update takes out of a club slot and restores later, or -1 when none is held. | Set to the record id in 0x85b820 Stadium::daily_update and reset to -1 there. Saved by 0x85bea0 Stadium::save_to_temp_file and loaded by 0x85ba40 Stadium::load_from_temp_file. The initial value is -1. | medium | sonnet | [0x85b820](../map/stadium.cpp.md) | [0x85b820](../map/stadium.cpp.md), [0x85ba40](../map/stadium.cpp.md), [0x85bea0](../map/stadium.cpp.md), [0x85c260](../map/stadium.cpp.md), [0x85c800](../map/stadium.cpp.md) |  |
| 0xa835ac | 4 | u32 | `g_stadium_default_attendance` | The fallback attendance that Stadium::calculate_match_attendance returns when it gets no match data, with an initial value of 15000. | Returned directly when param_1 is 0 in 0x85cba0 Stadium::calculate_match_attendance. No writer. The file value is 0x3a98, which is 15000. | medium | sonnet |  | [0x85cba0](../map/stadium.cpp.md) |  |
