# file_screens.cpp: 6 globals owned by file_screens.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a358 | 4 | float | `g_f32_146` | Read-only float constant 146. | the float at this address in .rdata is 146, and every access reads it | high | script |  | [0x590c00](../map/file_screens.cpp.md) |  |
| 0x96a35c | 4 | float | `g_f32_594` | Read-only float constant 594. | the float at this address in .rdata is 594, and every access reads it | high | script |  | [0x590c00](../map/file_screens.cpp.md) |  |
| 0x9c7a80 | 3 | char[3] | `g_str_chars_2e2e` | The text "..". | the bytes at this address are the text "..", and every access passes its address | high | script |  | [0x58f7c0](../map/file_screens.cpp.md) |  |
| 0x9c7a84 | 2 | char[2] | `g_str_chars_2e` | The text ".". | the bytes at this address are the text ".", and every access passes its address | high | script |  | [0x58f7c0](../map/file_screens.cpp.md) |  |
| 0xae2a34 | 2 | u16 | `g_save_summary_colour` | The colour value that create_save_file_summary_screen builds once with graphics_rgb_to_pixel. | Written only by 0x590c00 create_save_file_summary_screen from the result of 0x5e4800 graphics_rgb_to_pixel, on its first call. | medium | sonnet | [0x590c00](../map/file_screens.cpp.md) |  |  |
| 0xae2a36 | 1 | u8 | `g_save_summary_colour_init_flag` | The flag that records that create_save_file_summary_screen has built its static colour value. | Read and set only by 0x590c00 create_save_file_summary_screen before it writes g_save_summary_colour. | medium | sonnet | [0x590c00](../map/file_screens.cpp.md) | [0x590c00](../map/file_screens.cpp.md) |  |
