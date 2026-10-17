# Fine.cpp: 2 globals owned by Fine.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9cc03c | 17 | char[17] | `g_str_d_veckors_boter` | The text "%d veckors böter". | the bytes at this address are the text "%d veckors böter", and every access passes its address | high | script |  | [0x5a83e0](../map/Fine.cpp.md) |  |
| 0x9cc050 | 15 | char[15] | `g_str_1_veckas_boter` | The text "1 veckas böter". | the bytes at this address are the text "1 veckas böter", and every access passes its address | high | script |  | [0x5a83e0](../map/Fine.cpp.md) |  |
