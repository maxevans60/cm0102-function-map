# ire_prm.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x639bb0 | 161 (+2 unwind) | `IrePrm::IrePrm` | thiscall(IrePrm* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Irish Premier Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x639de0 | 11 | `IrePrm::`scalar deleting destructor'` | thiscall(IrePrm* this, unsigned flags), returns this, ret 4 | Runs the IrePrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x639e00 | 38 (+1 unwind) | `IrePrm::~IrePrm` | thiscall(IrePrm* this), ret 0 | Destroys the Irish Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x639e90 | 926 (+3 unwind) | `IrePrm::create_schedule` | thiscall(IrePrm* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the Premier Division round template for stage -1, with 36 rounds when ten clubs meet four times and 34 otherwise. | high | opus |  |
| 0x63a740 | 144 | `IrePrm::create_table` | thiscall(IrePrm* this), returns 1 on success and 0 on failure, ret 0 | Counts Premier Division clubs, accepts only ten or twelve, sets the meetings count to four or three, then fills the table and prize fund. | high | opus | 2026-10-16-research-name-check.md, wal-nir-irl.md |
| 0x63a900 | 42 | `IrePrm::set_up_rules` | thiscall(IrePrm* this), returns 1, ret 0 | Sets the Premier Division rule bytes, with the Irish First Division as the league below, and builds the schedule for stage -1. | high | opus |  |
| 0x63a9b0 | 134 | `IrePrm::start_new_season` | thiscall(IrePrm* this), ret 0 | Runs promotion and relegation, archives the stats, rebuilds rules, table and fixtures, and restarts the First Division. | high | opus |  |
| 0x63ab60 | 18 | `IrePrm::set_club_progress` | thiscall(IrePrm* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14, this unused | Stores a club's three progress codes in its Comp_Stats entry, mapping a code of 10 to 11 in the third one. | high | opus |  |
| 0x63aba0 | 22 | `IrePrm::get_fixed_draw_slot` | thiscall(IrePrm* this, Club* club) ret 4, returns char | Returns the fixed fixture draw slot stored for a club in the ten-entry table, or -1 when the club has none. | high | opus |  |
| 0x63abe0 | 53 | `IrePrm::set_fixed_draw_slot` | thiscall(IrePrm* this, Club* club, char slot) ret 8 | Stores a club's fixed draw slot in its entry, or in the first entry that is free or held by a club of another division. | high | opus |  |
| 0x63ac80 | 13 | `IrePrm::load_extra_data` | thiscall(IrePrm* this, FILE* file) ret 4, returns bool | Reads the ten fixed draw slot records from the save file and returns true when all ten arrive. | high | opus |  |
| 0x63acb0 | 9 | `IrePrm::save_extra_data` | thiscall(IrePrm* this, FILE* file) ret 4 | Writes the ten fixed draw slot records to the save file. | high | opus |  |
