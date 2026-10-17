# news.cpp: 5 globals owned by news.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xa654a0 | 3 | char[3] | `g_str_chars_3e20` | The text "> ". | the bytes at this address are the text "> ", and every access passes its address | high | script |  | [0x77bc80](../map/news.cpp.md) |  |
| 0xa65e94 | 72 | char[72] | `g_str_s_ar_borta_fran_spel_i_s_efter_att_han_f_a65e94` | The text "%s är borta från spel i %s efter att han fått %s under träningen i %ss.". | the bytes at this address are the text "%s är borta från spel i %s efter att han fått %s under träningen i %ss.", and every access passes its address | high | script |  | [0x77bc80](../map/news.cpp.md) |  |
| 0xa65edc | 71 | char[71] | `g_str_s_ar_borta_fran_spel_i_s_efter_att_han_f_a65edc` | The text "%s är borta från spel i %s efter att han fått %s under träningen i %s.". | the bytes at this address are the text "%s är borta från spel i %s efter att han fått %s under träningen i %s.", and every access passes its address | high | script |  | [0x77bc80](../map/news.cpp.md) |  |
| 0xa6648c | 87 | char[87] | `g_str_s_ar_borta_fran_spel_i_s_efter_att_han_f_a6648c` | The text "%s är borta från spel i %s efter att han fått %s i %s matchen mellan %s och %s den %s.". | the bytes at this address are the text "%s är borta från spel i %s efter att han fått %s i %s matchen mellan %s och %s den %s.", and every access passes its address | high | script |  | [0x77bc80](../map/news.cpp.md) |  |
| 0xb74344 | 4 | object | `g_news_work_object` | An object in the news file that NewsItem::write_text and the physio report click handler take in ECX. | Only its address is taken, by 0x77bc80 NewsItem::write_text and 0x7a2f10 physio_report_screen_handle_click. The class is not shown. | low | sonnet |  | [0x77bc80](../map/news.cpp.md), [0x7a2f10](../map/physio.cpp.md) |  |
