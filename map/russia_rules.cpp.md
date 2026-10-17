# russia_rules.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7ec770 | 31 (+1 unwind) | `RUSSIA_RULES::RUSSIA_RULES` | thiscall(RUSSIA_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Russia transfer rules, sets vtable 0x96f340 and builds its two transfer windows. | high | opus |  |
| 0x7ec7e0 | 77 | `RUSSIA_RULES::init_transfer_windows` | thiscall(RUSSIA_RULES *this) ret 0 | Allocates two 12-byte transfer windows for Russia, 15 December to 24 March and 28 June to 4 August, with rule set id 20. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7ec8e0 | 38 | `RUSSIA_RULES::get_loan_period` | thiscall(RUSSIA_RULES *this, int nation, int unused, char *out_month, short *out_year, char *out_stamp_month, short *out_stamp_year, int unused) ret 0x1c | Returns the month and year three months from today, plus the nation's contract date month and the year in which it falls next. | high | opus |  |
| 0x7ec950 | 17 | `RUSSIA_RULES::fill_squad_restrictions` | thiscall(RUSSIA_RULES *this, competition_t *competition, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and allows three foreign players in the competition at 0x9cf92c. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
