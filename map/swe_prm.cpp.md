# swe_prm.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x88fb10 | 219 (+2 unwind) | `SwePrm::SwePrm` | thiscall(SwePrm* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Swedish Premier Division on League, files clubs under the Second or Lower Division, then loads it or builds its table and fixtures. | high | opus |  |
| 0x88fe00 | 11 | `SwePrm::`scalar deleting destructor'` | thiscall(SwePrm* this, unsigned flags), returns this, ret 4 | Runs the SwePrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x88fe20 | 38 (+1 unwind) | `SwePrm::~SwePrm` | thiscall(SwePrm* this), ret 0 | Destroys the Swedish Premier Division, freeing its table, schedule at +0xba and Comp_Stats object before the League destructor runs. | high | opus |  |
| 0x88feb0 | 576 | `SwePrm::create_schedule` | thiscall(SwePrm* this, char stage, short* round_count, short* name_base, int* flag), returns schedule pointer, ret 0x10 | Builds the round dates of the 26-round Premier Division season from April to November for stage -1, and returns null for other stages. | high | opus |  |
| 0x890430 | 95 | `SwePrm::create_table` | thiscall(SwePrm* this), returns int, ret 0 | Allocates the 14-row table, fills it with the clubs of the Swedish Premier Division and sets the prize fund. | high | opus |  |
| 0x890550 | 43 | `SwePrm::set_up_rules` | thiscall(SwePrm* this), returns int, ret 0 | Sets the league rules of the Swedish Premier Division, with relegation to the First Division, and builds the base league schedule. | high | opus |  |
| 0x8905f0 | 158 | `SwePrm::start_new_season` | thiscall(SwePrm* this), ret 0 | Runs promotion and relegation through the Swedish pyramid, reassigns Second Division sections, then rebuilds the Premier Division and starts the lower divisions. | high | opus |  |
| 0x8907f0 | 122 | `SwePrm::process_promotion_relegation_chain` | thiscall(SwePrm* this, int pairwise), ret 4 | Records final positions and moves clubs between the Premier, First and Second Divisions and each Second Division section stage. | high | opus |  |
| 0x890980 | 143 | `swe_prm_promote_regional_clubs_to_first_division` | cdecl(void), ret 0 | When the Second Division is not playable, promotes three regional Second Division clubs to the First Division and sends relegated First Division clubs down. | medium | opus |  |
| 0x890b40 | 105 | `swe_prm_apply_second_division_moves` | cdecl(void), ret 0 | When the Second Division is playable, moves play-off winners into it, relegates its bottom clubs to the Lower Division and adds the twelve stored clubs. | medium | opus |  |
| 0x890c70 | 563 | `swe_prm_assign_second_division_sections` | cdecl(void), ret 0 | Deals the 72 Swedish Second Division clubs into six regional sections of twelve by location, filling a gap with one Lower Division club. | medium | opus |  |
| 0x891370 | 252 | `swe_prm_region_fit_score` | stdcall(Club* club, int section_id), returns int, ret 8 | Returns a 0 to 100 score for how well a club's city latitude and longitude fit one Swedish Second Division regional section. | medium | opus |  |
| 0x8916b0 | 23 | `SwePrm::set_club_progress` | stdcall(Club* club, char stage, char code1, char code2, char code3), ret 0x14 | Writes a club's three progress codes in its Comp_Stats entry, mapping codes 11 and 12 to 10 and 13 in the last two. | high | opus |  |
