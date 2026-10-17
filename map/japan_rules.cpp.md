# japan_rules.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x666bd0 | 31 (+1 unwind) | `JAPAN_RULES::JAPAN_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Japanese transfer rules on the TRANSFER_RULES base and builds its two transfer windows. | high | opus |  |
| 0x666c40 | 77 | `JAPAN_RULES::init_transfer_windows` | thiscall (this) ret 0 | Allocates and fills the two 12-byte Japanese transfer windows, showing an error box when the allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x666d40 | 91 | `JAPAN_RULES::can_sign_player` | thiscall (this, club_t *club, staff_t *player, int flag, date_t *date, u16 *reason or NULL) ret 0x14, returns 1 or 0 | Refuses a signing when the window is shut or a foreign player would take the club past five foreign players, then runs the base checks. | high | opus |  |
| 0x666e20 | 224 | `JAPAN_RULES::can_make_offer` | thiscall (this, transfer_offer_t *offer, club_t *club, date_t *date, u16 *reason or NULL) ret 0x10, returns 1 or 0 | Refuses a transfer offer that would leave the buying or selling club with more than five foreign players, then runs the base checks. | high | opus |  |
| 0x667090 | 10 | `JAPAN_RULES::fill_squad_restrictions` | thiscall (this, fixture_t *fixture, u8 *record_out) ret 8 | Fills the squad restriction record with 0xff and sets byte +2, a limit of three foreign players in the match squad. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
