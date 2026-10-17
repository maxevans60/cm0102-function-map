# poland_rules.cpp: 2 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7cd830 | 83 (+1 unwind) | `POLAND_RULES::POLAND_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5 forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the Poland transfer rules, sets vtable 0x96e61c, allocates one 12-byte transfer window and sets bytes +0x13 and +0x14 to 5. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7cd960 | 10 | `POLAND_RULES::fill_squad_restrictions` | thiscall (POLAND_RULES *this, squad_limits_t *out_limits) ret 8 | Clears the 42-byte match squad limits record to no limit and sets a limit of five foreign players. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
