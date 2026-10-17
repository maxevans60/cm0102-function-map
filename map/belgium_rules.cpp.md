# belgium_rules.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x424b90 | 34 (+1 unwind) | `BELGIUM_RULES::BELGIUM_RULES` | thiscall (BELGIUM_RULES *this, u8 rules_id, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Belgian transfer rules object, installs vtable 0x967c10, builds its three transfer windows and lifts the foreign and non-EU signing limits. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x424c00 | 93 | `BELGIUM_RULES::init_transfer_windows` | thiscall (BELGIUM_RULES *this) ret 0 | Allocates the three 12-byte Belgian transfer windows at +4, sets the count at +8 to 3 and fills their start and end dates. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x424d30 | 155 | `BELGIUM_RULES::can_sign_player` | thiscall (BELGIUM_RULES *this, club_t *buyer, staff_t *player, club_t *seller or NULL, int unused, date_t *date, u16 *out_reason) ret 0x14, returns 1 or 0 | Decides whether a Belgian club may sign a player, applying base squad limits in window 0 and league level rules in later windows. | high | opus |  |
| 0x424eb0 | 86 | `BELGIUM_RULES::can_make_offer` | thiscall (BELGIUM_RULES *this, TRANSFER_OFFER *offer, club_t *club, date_t *date, u16 *out_reason) ret 0x10 | Resolves the buying and selling clubs of a transfer offer and passes them, with the player, to the signing check of its own rules object. | high | opus |  |
| 0x424f80 | 11 | `BELGIUM_RULES::fill_squad_restrictions` | thiscall (BELGIUM_RULES *this, competition_t *competition unused, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and writes 21 at +6 and 2 at +8 for Belgian matches. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x424fa0 | 73 (+2 unwind) | `BELGIUM_RULES::post_deadline_news` | thiscall (BELGIUM_RULES *this, transfer_window_t *window, char deadline_state, date_t *date) ret 0xc | Posts a transfer deadline news item for Belgium with the state, window kind and date, skipping the deadline lifted item for the later windows. | high | opus |  |
| 0x4250b0 | 251 | `BELGIUM_RULES::write_deadline_news_text` | thiscall (BELGIUM_RULES *this, int unused, int nation_story, int unused2) ret 0xc | Writes the Belgian transfer deadline headline into the news text buffer, choosing the text from the deadline state and window kind slots. | high | opus |  |
| 0x425390 | 27 | `board_request_screen_open` | cdecl (club_index *club) ret 0 | Opens the Meet with Board screen for a club and clears the selected request parameters. | high | opus | 2026-10-16-stadium-research.md |
| 0x4253f0 | 292 (+1 unwind) | `board_request_screen_draw` | cdecl (void) ret 0 | Draws the Meet with Board screen, listing the six board request options for the club with Cancel and Confirm buttons. | high | opus | 2026-10-16-stadium-research.md |
| 0x4257f0 | 150 | `board_request_screen_handle_event` | cdecl (s16 event_id) ret 0, returns a screen result code | Handles board request screen events, storing a clicked request in param 1, submitting param 2 on event 9 and closing on event 8. | high | opus |  |
