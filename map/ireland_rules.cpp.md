# ireland_rules.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63c210 | 80 (+1 unwind) | `IRELAND_RULES::IRELAND_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Irish transfer rules on the TRANSFER_RULES base with one transfer window, reporting an error box when the allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x63c330 | 8 | `IRELAND_RULES::fill_squad_restrictions` | thiscall (this, fixture_t *fixture, u8 *record_out) ret 8 | Fills the 42-byte match squad restriction record with 0xff so that no foreign or non-EU limit applies. | high | opus | 2026-10-16-foreign-and-tactics-positions.md |
| 0x63c350 | 47 | `IRELAND_RULES::get_ineligibility_code` | thiscall (IRELAND_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns code 1 when a player already played for another club in one of three Irish competitions, else defers to the base check. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x63c3d0 | 94 | `IRELAND_RULES::can_loan_player` | thiscall (this, club_t *club, staff_t *player, char *message or NULL, u16 *reason or NULL) ret 0x10, returns 1 or 0 | Refuses a loan when the club already took five players on loan this season or both clubs play in the same division. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x63c4e0 | 21 | `IRELAND_RULES::record_loan` | thiscall (this, loan_record_t *loan) ret 4 | Adds one to the season loan count of the club named in the loan record when that club is Irish. | high | opus |  |
| 0x63c530 | 58 | `IRELAND_RULES::can_end_loan` | thiscall (this, club_t *club, staff_t *player, char *message or NULL, date_t *date or NULL, int unused) ret 0x14, returns 1 or 0 | Refuses to send back or recall a loan player while the Irish transfer window is shut, writing the matching message. | high | opus |  |
