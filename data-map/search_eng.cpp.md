# search_eng.cpp: 1 globals owned by search_eng.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xdd6bfc | 200 | char[200] | `g_search_staff_name_buffer` | Buffer that holds the formatted staff name while the search text is matched against it. | used only by 0x806080 search_text_matches_staff_name (high), which formats the name into it with length 200 and matches the search text | medium | sonnet |  | [0x806080](../map/search_eng.cpp.md) |  |
