# rus_prm.cpp: 13 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7eaa80 | 158 (+2 unwind) | `RusPrm::RusPrm` | thiscall(RusPrm* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Russian Premier League on League, then loads saved data or sets up rules, table, fixtures, sorted table and Comp_Stats. | high | opus |  |
| 0x7eaca0 | 11 | `RusPrm::`scalar deleting destructor'` | thiscall(RusPrm* this, unsigned flags), returns this, ret 4 | Runs the Russian Premier League destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7eacc0 | 38 (+1 unwind) | `RusPrm::~RusPrm` | thiscall(RusPrm* this), ret 0 | Destroys the Russian Premier League, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x7ead50 | 923 | `RusPrm::create_schedule` | thiscall(RusPrm* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 30-round league schedule, with other dates when Russia plays at a finals, or the one-round title play-off for stage 0. | high | opus |  |
| 0x7eb610 | 99 | `RusPrm::create_table` | thiscall(RusPrm* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 16-row table, fills it with the Russian Premier League clubs, sets the prize fund and pays each club 300000. | high | opus |  |
| 0x7eb740 | 46 | `RusPrm::set_up_rules` | thiscall(RusPrm* this), returns 1, ret 0 | Sets the Russian Premier League rule bytes, with no upper league and the First Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x7eb800 | 154 | `RusPrm::start_new_season` | thiscall(RusPrm* this), ret 0 | Runs Russian promotion and relegation, exchanges First and Second Division clubs, rebuilds table and fixtures and restarts the First Division. | high | opus |  |
| 0x7eba00 | 40 | `RusPrm::advance_stage` | thiscall(RusPrm* this), ret 0 | Moves the current stage index on by one and creates the title play-off when stage 0 starts, or reports an error past the last stage. | high | opus |  |
| 0x7eba90 | 133 (+1 unwind) | `RusPrm::create_title_playoff_stage` | thiscall(RusPrm* this), ret 0 | When the top two clubs finish level on points, builds a two-club Cup_Stage play-off for the title, else recalculates positions and statuses. | medium | opus |  |
| 0x7ebc40 | 144 | `RusPrm::update_staff_records_for_status` | thiscall(RusPrm* this, Club* club, char status, char stage, char* out_flag, Fixture* tie, int unused), returns int, ret 0x18 | For a play-off winner, puts the winning club above the loser in the table, then reruns the position update once no row has status 1. | high | opus |  |
| 0x7ebe20 | 258 | `rus_prm_exchange_first_and_second_division_clubs` | cdecl, no arguments, ret 0 | Promotes the strongest club of each pair of Russian second division zones to the first division and moves the bottom three first division clubs down. | high | sonnet |  |
| 0x7ec160 | 48 | `RusPrm::update_for_date` | thiscall(RusPrm* this, Date* today, int full_update), returns 1, ret 8 | Runs the base daily update, then at season end starts the title play-off stage if the top two clubs are level on points. | high | opus |  |
| 0x7ec1f0 | 9 | `RusPrm::save_extra_data` | thiscall(RusPrm* this, FILE* file), ret 4 | Writes the one-byte play-off pair count at +0xee to the saved game file. | high | opus |  |
