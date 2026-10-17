# european_awards.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x583280 | 19 | `EUROPE_RULES::EUROPE_RULES` | thiscall(EUROPE_RULES* this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14, returns this | Constructs the Europe-wide transfer rules object on the TRANSFER_RULES base, sets its vtable and clears a flag byte. | high | opus | 2026-10-16-sweep-rulebooks.md, 2026-10-16-sweep-season-end.md |
| 0x5832c0 | 8 | `TRANSFER_RULES::fill_squad_restrictions` | thiscall(TRANSFER_RULES* this, int unused, u8* record) ret 8 | Fills the 42-byte match squad restriction record with 0xff, the base default with no squad limits. | high | opus | 2026-10-16-foreign-and-tactics-positions.md |
| 0x5832e0 | 112 | `EUROPE_RULES::get_ineligibility_code` | thiscall(EUROPE_RULES* this, Staff* player, void* target) ret 8, returns code | Returns code 8 for some players in four listed competitions of the current season and set rounds, otherwise defers to the base eligibility check. | high | opus |  |
| 0x583400 | 36 (+1 unwind) | `EuropeanAwards::EuropeanAwards` | thiscall(EuropeanAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the European awards on NationAwards, sets its vtable and region bytes, then loads the awards from the file or creates them. | high | opus |  |
| 0x583470 | 1 | `shared_noop_ret4` | thiscall(void* this, one stack argument) ret 4 | Empty virtual body that pops one stack argument and returns, shared by competition, transfer rules, awards and ruling body vtables. | high | opus |  |
| 0x583480 | 163 (+4 unwind) | `EuropeanAwards::init_awards` | thiscall(EuropeanAwards* this, FILE* load_source or 0) ret 4 | Allocates the table of four European year awards and creates each YEAR_AWARD, reporting an error when the table allocation fails. | high | opus |  |
| 0x5836a0 | 96 (+1 unwind) | `EuropeanAwards::daily_update` | thiscall(EuropeanAwards* this, Date* date) ret 4 | On day 16 of month index 5, outside the 2001 season, gives the four European year awards from their top three nominees. | high | opus |  |
