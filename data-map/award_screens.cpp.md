# award_screens.cpp: 2 globals owned by award_screens.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xad9c68 | 2 | u16 | `g_award_team_dark_blue_pixel` | Pixel value for a dark blue text colour, made once by the team award screen. | 0x415f60 award_screen_draw_team_award stores the result of 0x5e4800 graphics_rgb_to_pixel for red 0, green 0, blue 0x40 and passes it as a text colour. | high | sonnet | [0x415f60](../map/award_screens.cpp.md) | [0x415f60](../map/award_screens.cpp.md), [0x416570](../map/award_screens.cpp.md) |  |
| 0xad9c6a | 1 | u8 | `g_award_team_dark_blue_pixel_ready` | Flag byte whose low bit is set once the dark blue pixel value has been made. | 0x415f60 award_screen_draw_team_award tests bit 0x10000 of the dword at 0xad9c68, which is bit 0 of this byte, before it creates the pixel. | medium | sonnet | [0x415f60](../map/award_screens.cpp.md) | [0x415f60](../map/award_screens.cpp.md) |  |
