# brazil_rules.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x43f0e0 | 83 (+1 unwind) | `BRAZIL_RULES::BRAZIL_RULES` | thiscall (BRAZIL_RULES *this, u8 rules_id, int nation_index, int continent_index, int arg4, int arg5) ret 0x14 | Constructs the Brazilian transfer rules object, installs vtable 0x968838, allocates one transfer window and sets the foreign signing limit to 3. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x43f210 | 56 | `BRAZIL_RULES::get_ineligibility_code` | thiscall (BRAZIL_RULES *this, staff_t *player, fixture_t *fixture) ret 8, returns a reason code, 0 when eligible | Returns 0 for friendlies and competition 0x9cf684, 4 when the player's competition stats entry names another club, otherwise the base code. | high | opus |  |
| 0x43f2a0 | 17 | `BRAZIL_RULES::fill_squad_restrictions` | thiscall (BRAZIL_RULES *this, competition_t *competition, u8 *record) ret 8 | Fills the 42-byte match squad restriction record with 0xff and allows two foreign players except in competition 0x9cf684. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
