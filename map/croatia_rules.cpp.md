# croatia_rules.cpp: 2 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x518500 | 80 (+1 unwind) | `CROATIA_RULES::CROATIA_RULES` | thiscall (CROATIA_RULES *this, u8 rules_id, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Croatian transfer rules object, installs vtable 0x969394 and allocates one transfer window from 1 June to 30 March. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x518620 | 10 | `CROATIA_RULES::fill_squad_restrictions` | thiscall (CROATIA_RULES *this, competition_t *competition unused, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and allows four foreign players. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
