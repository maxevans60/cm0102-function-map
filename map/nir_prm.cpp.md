# nir_prm.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x78e070 | 156 (+2 unwind) | `NirPrm::NirPrm` | thiscall(NirPrm* this, short comp_id, int owner) ret 8, returns this | Constructs the Northern Irish Premier Division on League, then loads saved data or sets up rules, table, fixtures, sort order, Comp_Stats and predictions. | high | opus |  |
| 0x78e280 | 11 | `NirPrm::`scalar deleting destructor'` | thiscall(NirPrm* this, unsigned flags) ret 4, returns this | Runs the NirPrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x78e2a0 | 38 (+1 unwind) | `NirPrm::~NirPrm` | thiscall(NirPrm* this) ret 0 | Destroys the Northern Irish Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x78e330 | 965 | `NirPrm::create_schedule` | thiscall(NirPrm* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns schedule pointer | Builds the 36-round schedule template of the Northern Irish Premier Division from mid August, with Christmas dates picked by the weekday of 1 December. | high | opus |  |
| 0x78ec60 | 95 | `NirPrm::create_table` | thiscall(NirPrm* this) ret 0, returns 1 or 0 when allocation fails or ten clubs are not found | Allocates the ten-row table, fills it with the Premier Division clubs and sets the prize fund. | high | opus |  |
| 0x78ed80 | 42 | `NirPrm::set_up_rules` | thiscall(NirPrm* this) ret 0, returns 1 | Sets the Premier Division rule bytes, with no upper league and the division in global 0x9cf8b4 below, and builds the season schedule. | high | opus |  |
| 0x78ee30 | 134 | `NirPrm::start_new_season` | thiscall(NirPrm* this) ret 0 | Runs promotion and relegation, archives the stats, rebuilds rules, table and fixtures, restarts the lower division and renews managers and officials. | high | opus |  |
| 0x78efe0 | 19 | `NirPrm::set_club_progress` | thiscall(NirPrm* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores a club's three progress codes in its Comp_Stats entry, mapping code 9 to 8 in the second and to 10 in the third. | high | opus |  |
