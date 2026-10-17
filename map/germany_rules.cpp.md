# germany_rules.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5dff70 | 31 (+1 unwind) | `GERMANY_RULES::GERMANY_RULES` | thiscall(GERMANY_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Germany transfer rules, sets vtable 0x96b3cc and builds its two transfer windows. | high | opus |  |
| 0x5dffe0 | 77 | `GERMANY_RULES::init_transfer_windows` | thiscall(GERMANY_RULES *this) ret 0 | Allocates two 12-byte transfer windows for Germany, 1 July to 15 August and 1 July to 15 January, with rule set id 10. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5e00e0 | 120 | `GERMANY_RULES::can_sign_player` | thiscall (GERMANY_RULES *this, club_t *buyer, staff_t *player, club_t *seller or NULL, Date *date, u16 *reason or NULL) ret 0x14, returns 1 or 0 | In the second German window, refuses German buyers outside two divisions and buys from a same nation club of lower level, else uses base checks. | high | opus |  |
| 0x5e0210 | 65 | `GERMANY_RULES::can_end_loan` | thiscall(GERMANY_RULES *this, club *club, player *player, char *msg, date_t *date, int flag) ret 0x14, returns bool | Refuses to end a loan between German clubs before it expires, writing the sent back or recalled text by which club asks. | high | opus |  |
| 0x5e02d0 | 19 | `GERMANY_RULES::fill_squad_restrictions` | thiscall(GERMANY_RULES *this, competition *comp, restriction_t *out) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets the non-EU limit to 3 for the competition at 0x9cf714, else 5. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x5e0310 | 73 (+2 unwind) | `GERMANY_RULES::post_deadline_news` | thiscall (GERMANY_RULES *this, transfer_window_t *window, char kind, s16 year) ret 0xc | Posts transfer deadline news item 0xfb2 to the managers of the rule set's nation, skipping kind 3 for windows of a nonzero type. | high | opus |  |
| 0x5e0420 | 195 | `GERMANY_RULES::write_deadline_news_text` | thiscall(GERMANY_RULES *this, int news, int rule_news, int arg3) ret 0xc | Writes the headline for a German window news item from its stage and window type, deferring to the base text when the flag is zero. | high | opus |  |
