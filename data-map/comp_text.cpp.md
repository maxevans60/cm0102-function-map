# comp_text.cpp: 2 globals owned by comp_text.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xadae17 | 1 | u8 | `g_text_wrap_line_buffer_lookbehind` | An alias into the wrapped text line buffers, five bytes before the buffer start, that Text::draw_wrapped uses to test for a hash character. | Read only by 0x4aeaf0 Text::draw_wrapped, which indexes it by line times 501 plus a column. That equals g_text_wrap_line_buffers at column minus 5. | low | sonnet |  | [0x4aeaf0](../map/comp_text.cpp.md) |  |
| 0xadae1c | 501 | buffer | `g_text_wrap_line_buffers` | The array of 501 byte line buffers that Text::draw_wrapped fills with the wrapped lines. | Only 0x4aeaf0 Text::draw_wrapped uses it, as the line buffer indexed by line number times 501. | medium | sonnet | [0x4aeaf0](../map/comp_text.cpp.md) | [0x4aeaf0](../map/comp_text.cpp.md) | 2026-10-14-clickable-names-inventory.md |
