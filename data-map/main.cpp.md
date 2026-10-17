# main.cpp: 2 globals owned by main.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xb67a28 | 4 | unknown | `g_single_instance_mutex` | The handle of the mutex that stops a second copy of the game from running. | written by 0x68d370 win_main (high) from CreateMutexA. Closed with CloseHandle by 0x68d370 win_main and 0x68dbc0 restart_game (high). | high | sonnet | [0x68d370](../map/main.cpp.md) | [0x68d370](../map/main.cpp.md), [0x68dbc0](../map/main.cpp.md) |  |
| 0xb67a3c | 4 | s32 | `g_synthetic_press_frames_left` | The count of message pump passes for which real mouse input stays blocked. A scrollbar key press sets it. | set by 0x5621f0 display_press_scrollbar_key (high). 0x68d520 pump_messages (high) counts it down and clears the left button flag at 0. 0x68d630 main_window_proc (high) ignores mouse messages while it is not 0. | medium | sonnet | [0x5621f0](../map/display.cpp.md), [0x68d520](../map/main.cpp.md) | [0x68d520](../map/main.cpp.md), [0x68d630](../map/main.cpp.md) | 2026-10-13-input-inventory.md, user32.c |
