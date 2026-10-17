# korea_rules.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x66e630 | 81 (+1 unwind) | `KOREA_RULES::KOREA_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the South Korean transfer rules on the TRANSFER_RULES base with one transfer window and a squad limit of seven foreign players. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x66e750 | 10 | `KOREA_RULES::fill_squad_restrictions` | thiscall (this, fixture_t *fixture, u8 *record_out) ret 8 | Fills the squad restriction record with 0xff and sets byte +0, a limit of three foreign players in the match squad. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x66e770 | 6 | `KOREA_RULES::get_ineligibility_code` | thiscall (this, staff_t *player, fixture_t *fixture) ret 8, returns reason code | Passes the player and fixture straight to the base match ineligibility check and returns its code. | high | opus |  |
