# physio.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7a1a70 | 4 | `physio_static_init` | cdecl(void) ret 0 | Registers the empty destructor of a physio.cpp static object with atexit at start-up. | medium | opus |  |
| 0x7a1a80 | 1 | `physio_static_object_destructor` | cdecl(void) ret 0 | Does nothing as the at-exit destructor of a physio.cpp static object. | medium | opus |  |
| 0x7a1a90 | 181 (+1 unwind) | `physio_file_report_news` | stdcall(Staff* physio, Staff* player) ret 8 | Assesses a player for a physio and files a type 0x1392 physio report news item to the physio's club manager. | high | opus |  |
| 0x7a1cd0 | 645 | `physio_write_report_news_text` | stdcall(NewsItem* item, Text* text, int is_body) ret 0xc | Writes the headline or the medical report body of a physio report news item from the assessment flags held in its slots. | high | opus |  |
| 0x7a25c0 | 55 | `physio_get_age_stage` | stdcall(Staff* player) ret 4, returns u8 stage code | Returns a career stage code for a player from his age against a peak age that depends on his main position. | medium | opus |  |
| 0x7a2650 | 241 | `physio_assess_player_fitness` | stdcall(Staff* physio, Staff* player, u16* flags_out, u8* recurring_type_out) ret 0x10 | Sets the physio report flags for a player's recurring injury, injury proneness, fitness approach and contact time, and outputs the recurring injury type. | medium | opus |  |
| 0x7a2900 | 99 | `physio_get_days_to_judge` | stdcall(Staff* physio, Staff* player) ret 8, returns int days | Returns the days a physio needs with a player before he can judge him, zero for top players and 180 on bad pointers. | medium | opus |  |
| 0x7a2a50 | 32 | `physio_report_screen_open` | cdecl(int *player_id, int *physio_id) ret 0 | Opens the Request Physio Report screen and stores the player and physio ids in screen parameters 0 and 1. | high | opus |  |
| 0x7a2ab0 | 341 (+1 unwind) | `physio_report_screen_build` | cdecl(void) ret 0 | Builds the Request Physio Report screen, listing the club physios of the player's club with Cancel and Confirm buttons. | high | opus |  |
| 0x7a2f10 | 145 | `physio_report_screen_handle_click` | cdecl(int object_index) ret 0, returns int screen result | Handles a click on the physio report screen: selects a physio, cancels, or confirms and files the report news. | high | opus |  |
