# library_without_asserts: 6 globals owned by library_without_asserts

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xad6aec | 3 | char[3] | `g_str_chars_5b5d` | The text "[]". | the bytes at this address are the text "[]", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
| 0xad6af0 | 2 | char[2] | `g_str_g_ad6af0` | The text "g". | the bytes at this address are the text "g", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
| 0xad6af4 | 3 | char[3] | `g_str_pq` | The text "pq". | the bytes at this address are the text "pq", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
| 0xad6b24 | 2 | char[2] | `g_str_z` | The text "z". | the bytes at this address are the text "z", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
| 0xad6b2c | 2 | char[2] | `g_str_7` | The text "7". | the bytes at this address are the text "7", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
| 0xad6b40 | 2 | char[2] | `g_str_f_ad6b40` | The text "f". | the bytes at this address are the text "f", and every access passes its address | high | script |  | [0x93b370](../map/library_without_asserts.md) |  |
