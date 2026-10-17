# argentina_rules.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x40a580 | 32 (+1 unwind) | `ARGENTINA_RULES::Argentina_rules` | thiscall(Argentina_rules* this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Argentine transfer rules on the TRANSFER_RULES base, sets its vtable, sets up its two windows and sets the foreign squad limit to 20. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x40a5f0 | 2 | `TRANSFER_RULES::rule_slot_5` | thiscall(TRANSFER_RULES* this, int a, int b, int c) ret 0xc | Returns 1 as the base default of TRANSFER_RULES vtable slot 5, which no country in 3.9.68 overrides. | low | opus |  |
| 0x40a600 | 2 | `TRANSFER_RULES::can_loan_player` | thiscall(TRANSFER_RULES* this, int player, int club, char* message_out, short* error_out) ret 0x10 | Returns 1 as the base default that allows a loan, for countries with no loan deadline. | high | opus |  |
| 0x40a610 | 2 | `TRANSFER_RULES::can_end_loan` | thiscall(TRANSFER_RULES* this, int a, int b, int c, char* message_out, short* error_out) ret 0x14 | Returns 1 as the base default that allows a loaned player to be recalled or sent back at any time. | high | opus |  |
| 0x40a620 | 77 | `ARGENTINA_RULES::init_transfer_windows` | thiscall(Argentina_rules* this) ret 0, ECX is this | Allocates and fills the two 12-byte Argentine transfer window records, flagging the second as limited, and reports an error box when allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x40a710 | 57 (+1 unwind) | `ARGENTINA_RULES::daily_update` | thiscall (ARGENTINA_RULES *this, Date *today) ret 4 | Clears byte 0 of every Argentine club's transfer counter record on the day before the second transfer window opens. | high | opus |  |
| 0x40a7d0 | 18 | `transfer_window_get_date` | thiscall (transfer_window_t *this, Date *out, s16 year) ret 8, returns out | Builds a Date from the weekday, day and month bytes at offsets 2 to 4 of a window record and a given year. | high | opus | 2026-10-16-sweep-rulebooks.md, 2026-10-16-sweep-season-end.md |
| 0x40a810 | 23 | `ARGENTINA_RULES::record_transfer` | thiscall(Argentina_rules* this, TRANSFER_OFFER* offer) ret 4 | Adds one to the window signing counter of the buying club when that club belongs to the rules nation. | high | opus |  |
| 0x40a860 | 58 | `ARGENTINA_RULES::can_sign_player` | thiscall(Argentina_rules* this, Club* club, int player, int arg3, Date* date, short* error_out) ret 0x14 | Refuses a bid with error 14 when a club with two signings bids in the limited window, else runs the base squad check. | high | opus |  |
| 0x40a900 | 109 | `ARGENTINA_RULES::can_make_offer` | thiscall(Argentina_rules* this, TRANSFER_OFFER* offer, Club* club, Date* date, short* error_out) ret 0x10 | Refuses a transfer with error 14 when it takes a club above two signings in the limited window, else runs the base check. | high | opus |  |
| 0x40aa10 | 10 | `ARGENTINA_RULES::fill_squad_restrictions` | thiscall(Argentina_rules* this, int fixture, u8* record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets a limit of four foreign players. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x40aa30 | 63 | `ARGENTINA_RULES::write_deadline_news_text` | thiscall(Argentina_rules* this, int a, int nation_flag, int c) ret 0xc | Writes the news that Argentine clubs may buy again with at most two signings before February, else posts the base deadline news. | high | opus |  |
