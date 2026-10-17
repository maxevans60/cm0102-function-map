# england_rules.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x579b30 | 80 (+1 unwind) | `ENGLAND_RULES::ENGLAND_RULES` | thiscall (ENGLAND_RULES *this, u8 rules_id, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the English transfer rules object, installs vtable 0x969f4c and allocates one transfer window from early June to a Thursday in late March. | high | opus | 2026-10-16-season-change-points.md, 2026-10-16-sweep-rulebooks.md |
| 0x579c50 | 10 | `ENGLAND_RULES::fill_squad_restrictions` | thiscall (ENGLAND_RULES *this, competition_t *competition unused, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and allows three non-EU players in every competition. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md, 2026-10-16-sweep-season-end.md |
| 0x579c70 | 73 (+1 unwind) | `ENGLAND_RULES::get_loan_period` | thiscall (ENGLAND_RULES *this, club_t *club, int arg, char *out_start_month, short *out_start_year, char *out_end_month, short *out_end_year, staff_t *player) ret 0x1c | Sets an English loan to three months from next month, but uses the base period after 19 June for players with byte +0x18 below 24. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x579d60 | 211 | `ENGLAND_RULES::can_loan_player` | thiscall (ENGLAND_RULES *this, club_t *club, staff_t *player, char *out_message or NULL, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses an English loan inside one league, past five loans a season, past two at once or outside the window, writing a message and reason. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x579fd0 | 21 | `ENGLAND_RULES::record_loan` | thiscall (ENGLAND_RULES *this, TRANSFER_OFFER *offer) ret 4 | Adds one to the season loan count of the borrowing club when that club is English. | high | opus |  |
| 0x57a020 | 37 | `ENGLAND_RULES::daily_update` | thiscall (ENGLAND_RULES *this, date_t *date) ret 4 | Resets the season loan count of every club in this rule set's nation when the date is 20 June. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x57a090 | 45 | `ENGLAND_RULES::get_ineligibility_code` | thiscall (ENGLAND_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns code 1 when a player is cup tied to another club in two English cup competitions, otherwise the base match eligibility code. | high | opus | 2026-10-16-sweep-rulebooks.md |
