# finland_rules.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5a9950 | 81 (+1 unwind) | `FINLAND_RULES::FINLAND_RULES` | thiscall(FINLAND_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Finland transfer rules, sets vtable 0x96a75c and allocates one 12-byte transfer window running from 16 November to 15 August. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5a9a80 | 38 | `FINLAND_RULES::get_loan_period` | thiscall (FINLAND_RULES *this, club_t *club, int arg, char *out_start_month, short *out_start_year, char *out_end_month, short *out_end_year, staff_t *player) ret 0x1c | Sets a loan to start next month and end at the season end month of the club's nation, this year or next. | high | opus |  |
| 0x5a9af0 | 62 | `FINLAND_RULES::can_loan_player` | thiscall(FINLAND_RULES *this, club *club, int unused, char *msg, u16 *out_error) ret 0x10, returns bool | Refuses a loan when no transfer window is open, writing the deadline text and error 9, and limits AI clubs to days 90 to 300. | high | opus |  |
| 0x5a9ba0 | 90 (+1 unwind) | `FINLAND_RULES::can_end_loan` | thiscall(FINLAND_RULES *this, club *club, player *player, char *msg, date_t *date, int flag) ret 0x14, returns bool | Refuses to end a loan between 18 August and 15 November, writing the sent back or recalled text by which club asks. | high | opus |  |
