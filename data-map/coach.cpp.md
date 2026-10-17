# coach.cpp: 3 globals owned by coach.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9689c8 | 8 | double | `g_f64_0_020833333333333332` | Read-only double constant 0.020833333333333332. | the double at this address in .rdata is 0.020833333333333332, and every access reads it | high | script |  | [0x48aff0](../map/coach.cpp.md) |  |
| 0x99aa40 | 232 | char[232] | `g_str_coach_unavailable_carpark_report_text` | The coach report text that says Keith Flannery is unavailable for training because he charges five pounds a car in the carpark. | 0x487f60 write_coach_report_news_text pushes this string as a text argument. The exe string starts with the coach name placeholder and mentions Keith Flannery and the carpark. | high | sonnet |  | [0x487f60](../map/coach.cpp.md) |  |
| 0xadadf4 | 4 | object | `g_coach_report_object` | A global object whose address goes into ECX when the coach report news is posted and when its text is written. | 0x48c290 coach_report_request_handle_action and 0x77bc80 NewsItem::write_text load its address before calls to 0x487c70 coach_post_report_news and 0x487f60 write_coach_report_news_text. | medium | sonnet |  | [0x48c290](../map/coach.cpp.md), [0x77bc80](../map/news.cpp.md) |  |
