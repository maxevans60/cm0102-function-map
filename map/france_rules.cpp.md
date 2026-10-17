# france_rules.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5c1570 | 31 (+1 unwind) | `FRANCE_RULES::FRANCE_RULES` | thiscall(FRANCE_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the France transfer rules, sets vtable 0x96ae48 and builds its three transfer windows. | high | opus |  |
| 0x5c15e0 | 93 | `FRANCE_RULES::init_transfer_windows` | thiscall(FRANCE_RULES *this) ret 0 | Allocates three 12-byte transfer windows for France, 30 May to 31 August, 1 September to 20 December and 21 December to 10 January. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5c1710 | 58 (+1 unwind) | `FRANCE_RULES::daily_update` | thiscall (FRANCE_RULES *this, Date *today) ret 4 | Clears bytes 0 and 1 of every French club's transfer counter record on the day before the second transfer window opens. | high | opus |  |
| 0x5c17d0 | 32 | `FRANCE_RULES::record_transfer` | thiscall(FRANCE_RULES *this, TRANSFER_OFFER *offer) ret 4 | Counts a completed signing by a French club, adding to the free transfer counter when offer +0x2f is set and to the purchase counter otherwise. | high | opus |  |
| 0x5c1830 | 100 | `FRANCE_RULES::can_sign_player` | thiscall(FRANCE_RULES *this, club *buyer, player *player, club *seller, date_t *date, u16 *out_error) ret 0x14, returns bool | Refuses a French club's purchase in the restricted window when it already bought one player or signed one free agent, else applies base squad checks. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5c1930 | 102 | `FRANCE_RULES::can_make_offer` | thiscall(FRANCE_RULES *this, TRANSFER_OFFER *offer, club *club, date_t *date, u16 *out_error) ret 0x10, returns bool | Refuses a transfer offer that would break the one purchase and one free transfer limit of the French restricted window, else applies base checks. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5c1a30 | 17 | `FRANCE_RULES::fill_squad_restrictions` | thiscall(FRANCE_RULES *this, competition *comp, restriction_t *out) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets the non-EU limit to 5 for the competition at 0x9cf5cc, else 3. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x5c1a70 | 72 (+2 unwind) | `FRANCE_RULES::post_deadline_news` | thiscall (FRANCE_RULES *this, transfer_window_t *window, char kind, s16 year) ret 0xc | Posts transfer deadline news item 0xfb2 to the managers of French clubs, except for windows of type 1. | high | opus |  |
| 0x5c1b90 | 281 | `FRANCE_RULES::write_deadline_news_text` | thiscall(FRANCE_RULES *this, int news, int rule_news, int arg3) ret 0xc | Writes the headline for a French window news item from its stage and window type, deferring to the base text when the flag is zero. | high | opus |  |
| 0x5c1ed0 | 58 | `FRANCE_RULES::can_end_loan` | thiscall(FRANCE_RULES *this, club *club, player *player, char *msg, date_t *date, int flag) ret 0x14, returns bool | Refuses to send back or recall a loan player while no French transfer window is open, writing the matching text. | high | opus |  |
