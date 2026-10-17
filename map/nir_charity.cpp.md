# nir_charity.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x789df0 | 129 (+2 unwind) | `NirCharity::NirCharity` | thiscall(NirCharity* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the Northern Irish charity cup, loads its saved state or picks its teams and builds its round table and Comp_Stats object. | high | opus |  |
| 0x789fb0 | 11 | `NirCharity::`scalar deleting destructor'` | thiscall(NirCharity* this, unsigned flags) ret 4, returns this | Destroys the Northern Irish charity cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x789fd0 | 62 (+1 unwind) | `NirCharity::~NirCharity` | thiscall(NirCharity* this) ret 0 | Restores the charity cup vtable, frees the team, round and tie arrays and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x78a0a0 | 98 | `NirCharity::create_round_table` | thiscall(NirCharity* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the single-round table of the charity match with its draw and match dates, for the whole-cup stage only. | high | opus |  |
| 0x78a1e0 | 165 | `NirCharity::select_teams` | thiscall(NirCharity* this) ret 0, returns 1 on success, 0 when a club is missing, -1 on allocation failure | Picks the league champion and the cup winner as the two teams, taking the league runner-up when one club won both. | high | opus |  |
| 0x78a410 | 125 | `NirCharity::start_new_season` | thiscall(NirCharity* this) ret 0 | Frees last season's charity cup data, archives the stats, moves the year on and picks the new teams and rounds. | high | opus |  |
