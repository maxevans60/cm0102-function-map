# nor_prm.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x791500 | 156 (+2 unwind) | `NorPrm::NorPrm` | thiscall(NorPrm* this, short year, Division* division) ret 8, returns this | Constructs the Norwegian Premier Division on League, then loads saved data or sets up rules, table, fixtures, sorting and its Comp_Stats object. | high | opus |  |
| 0x791710 | 11 | `NorPrm::`scalar deleting destructor'` | thiscall(NorPrm* this, unsigned flags) ret 4, returns this | Runs the NorPrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x791730 | 38 (+1 unwind) | `NorPrm::~NorPrm` | thiscall(NorPrm* this) ret 0 | Destroys the Norwegian Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7917c0 | 1560 (+8 unwind) | `NorPrm::create_schedule` | thiscall(NorPrm* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 26-round schedule template of the Norwegian Premier Division from April to October, with separate date sets for even and odd years. | high | opus |  |
| 0x7925e0 | 95 | `NorPrm::create_table` | thiscall(NorPrm* this) ret 0, returns 1 on success, 0 on failure | Allocates the 14-row table, fills it with the clubs of the Norwegian Premier Division and sets the prize fund. | high | opus |  |
| 0x792700 | 43 | `NorPrm::set_up_rules` | thiscall(NorPrm* this) ret 0, returns 1 | Sets the Norwegian Premier Division rule bytes, with no upper league and the First Division below, and builds the base schedule. | high | opus |  |
| 0x7927a0 | 138 | `NorPrm::start_new_season` | thiscall(NorPrm* this) ret 0 | Runs promotion and relegation for the Norwegian divisions, regroups the Second Division, rebuilds table and fixtures and starts the First Division season. | high | opus |  |
| 0x792960 | 156 | `nor_prm_swap_first_and_second_division_clubs` | cdecl(void) ret 0 | Promotes the top four Norwegian Second Division clubs to the First Division and moves relegated First Division clubs down to the Second Division. | medium | opus |  |
| 0x792b40 | 162 | `nor_prm_regroup_second_division_clubs` | cdecl(void) ret 0 | Sorts up to 96 Norwegian Second Division clubs from north to south and puts them in eight groups of twelve. | medium | opus |  |
| 0x792d40 | 19 | `NorPrm::set_club_progress` | thiscall(NorPrm* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, mapping code 12 to 11 in the second code and to 14 in the third. | high | opus |  |
