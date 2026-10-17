# ultimatum.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x9064a0 | 100 (+1 unwind) | `ultimatum_news_issue_ultimatum_action` | cdecl(News *news, int news_item_id) ret 0 | Finds the news item and opens the ultimatum confirm screen with the manager, ultimatum type, club and item id as parameters. | high | opus |  |
| 0x906610 | 175 | `ultimatum_screen_draw` | cdecl(void) ret 0, reads screen params 0 staff, 1 ultimatum type, 2 club | Draws the Please Confirm screen that asks whether the manager issues one of four ultimatum types to the club board, with Yes and No buttons. | high | opus |  |
| 0x906830 | 117 | `ultimatum_screen_handle_event` | cdecl(short area_index) ret 0, returns a screen result code | Handles the ultimatum confirm screen, issuing the ultimatum on Yes, closing on No, else passing menu bar events on. | high | opus |  |
