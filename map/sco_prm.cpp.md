# sco_prm.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7f0b80 | 165 (+2 unwind) | `ScoPrm::ScoPrm` | thiscall(ScoPrm* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Scottish Premier Division on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x7f0dd0 | 11 | `ScoPrm::`scalar deleting destructor'` | thiscall(ScoPrm* this, unsigned flags) ret 4, returns this | Runs the ScoPrm destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7f0df0 | 38 (+1 unwind) | `ScoPrm::~ScoPrm` | thiscall(ScoPrm* this) ret 0 | Destroys the Scottish Premier Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7f0e80 | 2686 | `ScoPrm::create_schedule` | thiscall(ScoPrm* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 36-round 1999 schedule or the 38-round later schedule for stage -1, and five-round schedules for the two split stages 0 and 1. | high | opus |  |
| 0x7f2820 | 108 | `ScoPrm::create_table` | thiscall(ScoPrm* this) ret 0, returns 1 on success and 0 on failure | Allocates the 10-row, later 12-row, table, fills it with Scottish Premier Division clubs, sets the prize fund and pays each club 500000. | high | opus |  |
| 0x7f2970 | 59 | `ScoPrm::set_up_rules` | thiscall(ScoPrm* this) ret 0, returns 1 | Sets the Scottish Premier Division rule bytes, with no upper league and the First Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x7f2a70 | 217 | `ScoPrm::start_new_season` | thiscall(ScoPrm* this) ret 0 | Runs the Scottish promotion and relegation step, rebuilds rules, table and fixtures, then restarts the First, Second and Third Divisions. | high | opus |  |
| 0x7f2d20 | 36 | `ScoPrm::update_for_date` | thiscall(ScoPrm* this, Date* today, int full_update) ret 8 | Creates the split stages once every club has played 33 games in the three-stage season, then runs the League daily update. | high | opus |  |
| 0x7f2d90 | 207 (+2 unwind) | `ScoPrm::create_split_stages` | thiscall(ScoPrm* this) ret 0 | Copies the top six and bottom six table clubs into two League_Stage objects with the split schedules, then sets four stages and the split comparator. | high | opus |  |
| 0x7f3010 | 36 | `ScoPrm::update_staff_records_for_status` | thiscall(ScoPrm* this, Club* club, char status, char stage, int a4, Fixture* fixture, int a6) ret 0x18, returns 0 | Adds the staff record for a Premier Division champion, a club that qualifies for the championship group, or a relegated club in the main stage. | high | opus |  |
| 0x7f3080 | 114 | `ScoPrm::build_fate_news_text` | thiscall(ScoPrm* this, int club_index, char fate, char stage, int a4, int a5, int a6, int a7, int a8, int full_sentence, int a10) ret 0x28 | Writes the news that a club qualifies for the championship group stage of the Premier Division, and defers other fates to the Comp base. | high | opus |  |
| 0x7f31c0 | 32 | `ScoPrm::set_club_progress` | thiscall(ScoPrm* this, Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, mapping code 10 to 9 and fixing the third code in 1999. | high | opus |  |
| 0x7f3220 | 19 | `sco_prm_compare_split_half` | cdecl(const TableRow* a, const TableRow* b) ret 0, returns int | Compares two table rows by split half, putting rows whose position byte is above five after the top six, for table sorting. | medium | opus |  |
