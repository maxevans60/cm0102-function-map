# coach.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x487c50 | 4 | `coach_init_static_global` | cdecl, no arguments, ret 0 | Registers the empty exit routine at 0x487c60 with atexit during start-up for a static global of coach.cpp. | high | opus |  |
| 0x487c60 | 1 | `coach_exit_static_global` | cdecl, no arguments, ret 0 | Runs the empty destructor of a static global of coach.cpp at program exit and does nothing. | medium | opus |  |
| 0x487c70 | 237 (+1 unwind) | `coach_post_report_news` | stdcall(Staff* coach, Staff* player) ret 8 | Assesses a player for a coach and posts a coach report news item with 23 slots to the coach's club. | high | opus |  |
| 0x487f60 | 3475 | `write_coach_report_news_text` | stdcall(NewsItem* item, int full_text, Text* out) ret 0xc | Writes the coach report news text from the news slots, choosing wording by career stage and verdict flags. | high | opus |  |
| 0x48af30 | 71 | `coach_get_player_career_stage` | stdcall(Staff* player) ret 4, returns a flag byte | Returns a career stage flag for a player: 1 under 18, 2 under 24, 4 veteran, 8 journeyman or 16 established. | medium | opus |  |
| 0x48aff0 | 786 (+1 unwind) | `coach_assess_player` | stdcall(Staff* coach, Staff* player, ushort* verdict_a, ushort* verdict_b) ret 0x10 | Judges a player for a coach's report and sets two verdict flag words from ability, potential, role scores and squad status. | high | opus |  |
| 0x48ba10 | 155 | `coach_get_assessment_days` | stdcall(Staff* coach, Staff* player) ret 8, returns days | Returns how many days a coach needs at the club to judge a player, fewer for better coaches and zero for obvious stars. | medium | opus |  |
| 0x48bc00 | 102 | `coach_open_report_request_screen` | cdecl(Staff* player, Staff* coach), ret 0 | Opens the Request Coach Report screen and stores the player, the selected coach bit and the club as screen parameters. | high | opus |  |
| 0x48bd20 | 422 (+1 unwind) | `coach_report_request_draw` | cdecl(void), ret 0 | Draws the Request Coach Report screen with the player name, a tick list of club coaches, Select All, Cancel and Confirm. | high | opus |  |
| 0x48c290 | 264 | `coach_report_request_handle_action` | cdecl(int item), returns action code, ret 0 | Handles a click on the Request Coach Report screen: toggles one coach, selects all, or sends the report request to each ticked coach. | high | opus |  |
