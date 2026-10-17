# discipline.cpp: 1 globals owned by discipline.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9c36c0 | 40 | char[40] | `g_str_overklaga_s_dom_pa_1_match_avstangning` | The text "Överklaga %s dom på 1 match avstängning". | the bytes at this address are the text "Överklaga %s dom på 1 match avstängning", and every access passes its address | high | script |  | [0x55ea10](../map/discipline.cpp.md) |  |
