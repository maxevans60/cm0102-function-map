# northern_ireland_rules.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7936d0 | 80 (+1 unwind) | `NORTHERN_IRELAND_RULES::NORTHERN_IRELAND_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5 forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the Northern Ireland transfer rules, sets vtable 0x96df9c and allocates one 12-byte transfer window, with an error box when allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7937f0 | 47 | `NORTHERN_IRELAND_RULES::get_ineligibility_code` | thiscall (NORTHERN_IRELAND_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns code 1 when the player is tied to another club in one of three cup competitions, else uses the base match eligibility check. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x793870 | 51 | `NORTHERN_IRELAND_RULES::get_loan_period` | thiscall (NORTHERN_IRELAND_RULES *this, club_t *club, int arg, char *out_start_month, short *out_start_year, char *out_end_month, short *out_end_year, staff_t *player) ret 0x1c | Sets the loan start three months ahead and the end at the season end month, and moves the start back to the end when later. | high | opus |  |
| 0x793900 | 16 | `NORTHERN_IRELAND_RULES::can_loan_player` | thiscall (NORTHERN_IRELAND_RULES *this, int unused, person *player, char *out_message, u16 *out_reason) ret 0x10, returns 1 | Always allows a loan, caching the player's contract in the global contract pointer 0xae1080 for later checks. | high | opus |  |
