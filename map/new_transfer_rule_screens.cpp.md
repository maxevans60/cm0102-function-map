# new_transfer_rule_screens.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x77b700 | 85 (+1 unwind) | `transfer_rules_info_screen_open` | cdecl(int news_id, int news_arg) ret 0 | Opens the transfer regulations information screen at the overview page and, when a news item is given, passes its slot as the second screen parameter. | high | opus |  |
| 0x77b850 | 201 (+1 unwind) | `transfer_rules_info_screen_display` | cdecl() ret 0 | Draws the transfer regulations information screen with the proposed or current title, four page tabs and the text of the selected page. | high | opus | 2026-10-16-sweep-season-end.md |
| 0x77bb30 | 56 | `transfer_rules_info_screen_handle_click` | cdecl(short cell) ret 0, returns int screen result code | Handles a click on the transfer regulations screen, switching page on a tab cell and passing other clicks to the menu bar handlers. | high | opus | 2026-10-16-sweep-season-end.md |
