# greece_rules.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5eceb0 | 32 (+1 unwind) | `GREECE_RULES::GREECE_RULES` | thiscall(GREECE_RULES *this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Greece transfer rules, sets vtable 0x96b784, builds its two transfer windows and sets byte +0x14 to 6. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5ecf20 | 77 | `GREECE_RULES::init_transfer_windows` | thiscall(GREECE_RULES *this) ret 0 | Allocates two 12-byte transfer windows for Greece, 22 May to 29 August and 1 January to 20 January, with rule set id 11. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x5ed020 | 19 | `GREECE_RULES::fill_squad_restrictions` | thiscall(GREECE_RULES *this, competition *comp, restriction_t *out) ret 8 | Fills the 42-byte match squad restriction record with 0xff and sets the non-EU limit to 5 for the competition at 0x9cf86c, else 4. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
| 0x5ed060 | 2 | `GREECE_RULES::can_loan_player` | thiscall(GREECE_RULES* this, int a, int b, char* message_out, short* error_out) ret 0x10, returns 1 | Allows every loan by returning true, shared as the loan check slot of the Greece, Croatia and Poland rules. | high | opus |  |
