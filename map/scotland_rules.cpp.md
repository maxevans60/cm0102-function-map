# scotland_rules.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7f6390 | 82 (+1 unwind) | `SCOTLAND_RULES::SCOTLAND_RULES` | thiscall(SCOTLAND_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Scotland transfer rules, sets vtable 0x96f838 and builds one transfer window from 30 May to 30 March, with rule set id 21. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7f64c0 | 37 | `SCOTLAND_RULES::fill_squad_restrictions` | thiscall(SCOTLAND_RULES *this, fixture_t *fixture, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets an age rule or a squad limit for two Scottish competitions. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x7f6530 | 58 | `SCOTLAND_RULES::get_loan_period` | thiscall(SCOTLAND_RULES *this, int nation, int unused, char *out_start_month, short *out_start_year, char *out_end_month, short *out_end_year, staff_t *player) ret 0x1c | Starts a Scottish loan next month and ends it at the season end month for players under 22, otherwise three months later. | high | opus |  |
| 0x7f65d0 | 52 | `SCOTLAND_RULES::get_ineligibility_code` | thiscall(SCOTLAND_RULES *this unused, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns code 1 when a player played for another club in one of two Scottish cup competitions, otherwise the base match eligibility code. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7f6650 | 71 | `SCOTLAND_RULES::can_loan_player` | thiscall(SCOTLAND_RULES *this unused, club_t *club, staff_t *player, char *out_message, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses a loan between two clubs of the Scottish competition at 0x9cf5dc, writing a message and reason 0x1d. | high | opus | 2026-10-16-sweep-rulebooks.md |
