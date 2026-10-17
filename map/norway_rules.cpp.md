# norway_rules.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7944f0 | 80 (+1 unwind) | `NORWAY_RULES::NORWAY_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5 forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the Norway transfer rules, sets vtable 0x96dfe4 and allocates one 12-byte transfer window, with an error box when allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x794610 | 95 (+1 unwind) | `NORWAY_RULES::get_ineligibility_code` | thiscall (NORWAY_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns 5 when the player's date at +0x3e is after the first window closes, 2 within three days of that date, else the base code. | high | opus |  |
| 0x794740 | 10 | `NORWAY_RULES::fill_squad_restrictions` | thiscall (NORWAY_RULES *this, squad_limits_t *out_limits) ret 8 | Clears the 42-byte match squad limits record to no limit and sets a limit of two non-EU players. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x794760 | 41 | `NORWAY_RULES::can_loan_player` | thiscall (NORWAY_RULES *this, int unused, int unused2, char *out_message, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses a loan outside the open transfer window, writing the loan deadline passed text and reason code 9. | high | opus |  |
| 0x7947d0 | 71 (+2 unwind) | `NORWAY_RULES::post_deadline_news` | thiscall (NORWAY_RULES *this, transfer_window_t *window, char kind, s16 year) ret 0xc | Posts transfer deadline news item 0xfb2 to the managers of Norwegian clubs, except for kind 3. | high | opus |  |
| 0x7948e0 | 167 | `NORWAY_RULES::write_deadline_news_text` | thiscall (NORWAY_RULES *this, int news_item, u32 arg) ret 0xc | Writes the Norwegian transfer deadline news text for the passed, last day and next week states, else uses the base text. | high | opus |  |
