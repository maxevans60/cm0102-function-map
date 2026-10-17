# news_screens.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x788010 | 151 | `news_screens_open_news_screen` | cdecl(Screen* screen, int initial_item) ret 0 | Pushes the news screen with its build, input and exit handlers and sets its screen parameters, including a 30-byte filter text buffer. | high | opus | 2026-10-14-assistant-and-days-inventory.md, 2026-10-14-clickable-names-inventory.md, 2026-10-14-game-creation-inventory.md |
| 0x7881e0 | 1244 (+5 unwind) | `news_screens_build_news_screen` | cdecl(void) ret 0 | Builds the manager news screen with the category tabs, filter, paged news item list, selected item text and Next Unread button. | high | opus | 2026-10-14-clickable-names-inventory.md, 2026-10-14-game-creation-inventory.md, build-brief-0.3.0.md, waits.c |
| 0x789280 | 9 | `NewsItem::get_date` | thiscall(NewsItem* this, Date* out) ret 4 | Copies the eight-byte date of a news item into the caller's Date. | medium | opus |  |
| 0x7892b0 | 402 | `news_screens_news_input` | cdecl(short widget or -1) ret 0, returns screen code | Handles input on the news screen, switching tabs, opening items and Next Unread, and passes other clicks to the side bar handlers. | high | opus | 2026-10-14-assistant-and-days-inventory.md, 2026-10-14-clickable-names-inventory.md, 2026-10-14-game-creation-inventory.md |
| 0x7897a0 | 22 | `news_screens_news_exit` | cdecl(void) ret 0 | Frees the cached news item list of the news screen and clears its two screen parameters on leaving the screen. | high | opus | 2026-10-14-clickable-names-inventory.md, 2026-10-14-game-creation-inventory.md |
| 0x7897f0 | 34 | `news_screens_open_send_message` | cdecl(Staff* recipient or 0, int context) ret 0 | Opens the send message screen for one manager or for all, allocating a 101-byte text buffer as a screen parameter. | high | opus |  |
| 0x789860 | 84 (+1 unwind) | `news_screens_reply_to_news_item` | cdecl(int item_id, int context) ret 0 | Opens the send message screen addressed to the sender of a news item, or to all managers when the item has no sender. | medium | opus |  |
| 0x789990 | 166 | `news_screens_build_send_message` | cdecl(void) ret 0 | Builds the send message screen with the recipient title, a text entry box and the Cancel and Send buttons. | high | opus |  |
| 0x789bb0 | 175 (+1 unwind) | `news_screens_send_message_input` | cdecl(short widget or -1) ret 0, returns screen code | Handles the send message screen, queueing a type 5000 message to the recipient or every human manager on Send, and closing on Cancel. | high | opus |  |
