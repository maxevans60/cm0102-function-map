# History.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5f11c0 | 121 | `history_screen_open` | cdecl(const char* his_name) ret 0 | Opens the history text screen with its draw, event and free callbacks and seeds its layout and the .his file name. | high | opus |  |
| 0x5f1360 | 678 | `history_screen_draw` | cdecl(void) ret 0 | Draws the history text screen, loads the .his file on first entry, and word-wraps each section into list rows. | high | opus |  |
| 0x5f1ba0 | 132 | `history_screen_handle_event` | cdecl(short area_index, -1 for none) ret 0, returns a screen result code | Handles history screen events, updates the picture for the selected section, and follows a section link or closes the screen. | high | opus |  |
| 0x5f1d60 | 86 | `history_screen_free` | cdecl(void) ret 0 | Frees the title, picture and section tables that the .his loader stored in the history screen parameters. | high | opus |  |
| 0x5f1e50 | 520 | `history_load_his_file` | cdecl(const char* his_name, int unused) ret 0, returns bool | Parses a .his history file into title, section and picture tables and stores them in the history screen parameters. | high | opus |  |
| 0x5f2500 | 34 | `history_his_file_exists` | cdecl(const char* his_name) ret 0, returns 1 or 0 | Returns whether a named .his file exists in cm3_history, only when the game mode at 0xae3138+8 is 0 or 1. | high | opus |  |
| 0x5f2580 | 117 | `history_get_his_file_category` | cdecl(const char* his_name) ret 0, returns category index or -1 | Reads the cat or category tag of a .his file and returns its index in the history category name table, or -1. | high | opus |  |
| 0x5f2700 | 97 | `history_get_his_file_title` | cdecl(const char* his_name) ret 0, returns char* to a static buffer or NULL | Reads the title tag of a named .his file into a static buffer and returns it, or NULL when the file has none. | high | opus |  |
| 0x5f2840 | 242 | `verify_history_files` | cdecl(void) ret 0 | Checks every .his file in CM3_HISTORY against the nations, clubs, competitions, staff and history categories, and reports mismatches. | high | opus |  |
| 0x5f2b80 | 36 | `history_written_screen_open` | cdecl(int category) ret 0 | Opens the written history screen for a category with its draw, click and close callbacks. | high | opus |  |
| 0x5f2c00 | 405 (+1 unwind) | `history_written_screen_draw` | cdecl(void) ret 0 | Draws the written history screen with category tabs and a sorted list of the .his file titles of the chosen category. | high | opus |  |
| 0x5f3030 | 118 | `history_written_screen_draw_fragment_5f3030` | not a function entry: address falls inside an instruction of 0x5f2c00, no own convention | Marks a false entry inside the written history screen builder at 0x5f2c00, found through a stray data value at 0xaa2094. | high | opus |  |
| 0x5f31c0 | 167 | `history_written_screen_handle_click` | cdecl(short widget_index) ret 0, returns -0xb when handled or the menubar handler result | Handles a click on the written history screen: picks a category, opens a chosen history file, or passes other clicks to the menubar. | high | opus |  |
| 0x5f33d0 | 19 | `history_written_screen_close` | cdecl(void) ret 0 | Frees the buffer in screen parameter one and clears screen parameters one and two when the written history screen closes. | high | opus |  |
| 0x5f3410 | 19 | `history_compare_entries_by_title` | cdecl(HistoryEntry* a, HistoryEntry* b) ret 0, returns int | Compares two history list entries by their titles at +0x104 for qsort, ordering null entries last. | high | opus |  |
