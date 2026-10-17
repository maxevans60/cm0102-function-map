# australia_rules.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x412c80 | 82 (+1 unwind) | `AUSTRALIA_RULES::Australia_rules` | thiscall(Australia_rules* this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Australian transfer rules with one 12-byte transfer window and a foreign squad limit of six. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x412db0 | 10 | `AUSTRALIA_RULES::fill_squad_restrictions` | thiscall(Australia_rules* this, int fixture, u8* record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets a limit of six foreign players. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x412dd0 | 41 | `AUSTRALIA_RULES::can_loan_player` | thiscall(Australia_rules* this, int player, int club, char* message_out, short* error_out) ret 0x10 | Refuses a loan with error 9 and a deadline message when today is outside every transfer window of the rules. | high | opus |  |
