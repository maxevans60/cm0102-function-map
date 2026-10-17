# spain_rules.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x859400 | 32 (+1 unwind) | `SPAIN_RULES::SPAIN_RULES` | thiscall(SPAIN_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Spain transfer rules, sets vtable 0x96fdec, builds its two transfer windows and sets byte +0x14 to 6. | high | opus | 2026-10-16-season-change-points.md, 2026-10-16-sweep-rulebooks.md |
| 0x859470 | 77 | `SPAIN_RULES::init_transfer_windows` | thiscall(SPAIN_RULES *this) ret 0 | Allocates two 12-byte transfer windows for Spain, 17 June to 20 August and 15 December to 31 January, with rule set id 22. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x859570 | 35 | `SPAIN_RULES::fill_squad_restrictions` | thiscall(SPAIN_RULES *this, competition_t *competition, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets the non-EU limit to 2, 3 or 4 by competition and season. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-research-name-check.md, 2026-10-16-sweep-rulebooks.md, spa.md |
| 0x8595e0 | 28 | `SPAIN_RULES::get_ineligibility_code` | thiscall(SPAIN_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns 0 when the fixture has no competition, is a friendly or is the competition at 0x9cf684, otherwise the base eligibility code. | high | opus |  |
| 0x859630 | 111 | `SPAIN_RULES::can_loan_player` | thiscall(SPAIN_RULES *this, club_t *club, staff_t *player, char *out_message, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses a Spanish loan outside the window with reason 9, or between clubs of one division after five league games with reason 0x1f. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x859780 | 84 | `SPAIN_RULES::can_sign_player` | thiscall(SPAIN_RULES *this unused, club_t *buyer, staff_t *player, club_t *seller, date_t *date, u16 *out_reason) ret 0x14, returns 1 or 0 | Refuses a foreign signing by a club outside two Spanish divisions with reason 0x15, and any signing outside the window with reason 9. | high | opus |  |
| 0x859850 | 212 | `SPAIN_RULES::can_make_offer` | thiscall(SPAIN_RULES *this unused, TRANSFER_OFFER *offer, club_t *club, date_t *date, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses an offer outside the window with reason 9, or one adding foreign players to a club outside two Spanish divisions with reason 0x15. | high | opus |  |
