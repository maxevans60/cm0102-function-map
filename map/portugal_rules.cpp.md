# portugal_rules.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7d3d80 | 31 (+1 unwind) | `PORTUGAL_RULES::PORTUGAL_RULES` | thiscall (this, u8 flag, int nation_index, int continent_index, int arg4, int arg5 forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the Portugal transfer rules, sets vtable 0x96e9c0 and sets up its two transfer windows. | high | opus |  |
| 0x7d3df0 | 77 | `PORTUGAL_RULES::init_transfer_windows` | thiscall (PORTUGAL_RULES *this in ECX) ret 0 | Allocates and fills the two 12-byte Portuguese transfer windows, with an error box when allocation fails. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7d3ef0 | 123 | `PORTUGAL_RULES::can_sign_player` | thiscall (PORTUGAL_RULES *this, club *buyer, person *player, int arg3, date_t *date, u16 *out_reason) ret 0x14, returns 1 or 0 | Refuses a signing outside the transfer window or when it puts the club over its non-EU foreign player limit, else uses the base check. | high | opus |  |
| 0x7d4040 | 314 | `PORTUGAL_RULES::can_make_offer` | thiscall (PORTUGAL_RULES *this, TRANSFER_OFFER *offer, club *club, date_t *date, u16 *out_reason) ret 0x10, returns 1 or 0 | Checks a transfer offer and its extra players against the transfer window and the Portuguese non-EU player limit, else uses the base check. | high | opus |  |
| 0x7d43c0 | 20 | `PORTUGAL_RULES::fill_squad_restrictions` | thiscall (PORTUGAL_RULES *this, fixture *match, squad_limits_t *out_limits) ret 8 | Clears the 42-byte match squad limits record and sets three non-EU players for competition 0x9cf7c0, else four. | high | opus | 2026-10-16-foreign-and-tactics-positions.md, 2026-10-16-sweep-rulebooks.md |
