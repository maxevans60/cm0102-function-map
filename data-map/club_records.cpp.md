# club_records.cpp: 4 globals owned by club_records.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x968920 | 8 | double | `g_f64_0_08` | Read-only double constant 0.08. | the double at this address in .rdata is 0.08, and every access reads it | high | script |  | [0x444930](../map/club_records.cpp.md), [0x846920](../map/shortlist_manager.cpp.md) |  |
| 0x968948 | 8 | double | `g_f64_minus_1_0` | Read-only double constant -1.0. | the double at this address in .rdata is -1.0, and every access reads it | high | script |  | [0x447880](../map/club_records.cpp.md), [0x4496d0](../map/club_records.cpp.md), [0x449810](../map/club_records.cpp.md), [0x44c650](../map/club_records.cpp.md), [0x450d50](../map/club_records.cpp.md), [0x452a90](../map/club_records.cpp.md) and 6 more |  |
| 0x98c014 | 2 | char[2] | `g_str_chars_3f` | The text "?". | the bytes at this address are the text "?", and every access passes its address | high | script |  | [0x449810](../map/club_records.cpp.md), [0x4a5690](../map/comp_screens.cpp.md) |  |
| 0x98c160 | 120 | char[120] | `g_str_s_gate_receipts_e_g_pound_1_000_000_v_s` | The text "<%s - gate receipts(e.g.£1,000,000)> v {}<%s - opposition team> {}<%s - fixture name e.g. FA Cup Final>{} {}<%s - date>". | the bytes at this address are the text "<%s - gate receipts(e.g.£1,000,000)> v {}<%s - opposition team> {}<%s - fixture name e.g. FA Cup Final>{} {}<%s - date>", and every access passes its address | high | script |  | [0x449810](../map/club_records.cpp.md) |  |
