# weather.cpp: 1 globals owned by weather.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xad4e94 | 28 | char[28] | `g_str_d_temperature_eg_2_degree_c` | The text "<%d - Temperature eg -2 >°C". | the bytes at this address are the text "<%d - Temperature eg -2 >°C", and every access passes its address | high | script |  | [0x9233a0](../map/weather.cpp.md) |  |
