# turkey_rules.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x9020a0 | 83 (+1 unwind) | `TURKEY_RULES::TURKEY_RULES` | thiscall(TURKEY_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Turkey transfer rules, sets vtable 0x97075c and builds one transfer window from 1 June to 31 January, with rule set id 24. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x9021d0 | 33 | `TURKEY_RULES::fill_squad_restrictions` | thiscall(TURKEY_RULES *this, competition_t *competition, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets six or no foreign players, or an age rule, by competition. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x902240 | 55 | `TURKEY_RULES::can_loan_player` | thiscall(TURKEY_RULES *this, club_t *club, staff_t *player, char *out_message, u16 *out_reason) ret 0x10, returns 1 or 0 | Refuses a loan with reason 9 and a deadline message when today is outside every transfer window of the rules. | high | opus |  |
