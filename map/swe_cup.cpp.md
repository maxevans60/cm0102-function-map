# swe_cup.cpp: 15 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x88cbb0 | 169 (+2 unwind) | `SweCup::SweCup` | thiscall(SweCup* this, short year, Nation* nation) ret 8 | Constructs the Swedish cup on Cup, then loads saved data or builds the entrants, rounds, fixture tree, stats, seven preliminary stages and ranking. | high | opus |  |
| 0x88ce00 | 11 | `SweCup::`scalar deleting destructor'` | thiscall(SweCup* this, unsigned flags) ret 4 | Runs the Swedish cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x88ce20 | 90 (+1 unwind) | `SweCup::~SweCup` | thiscall(SweCup* this) ret 0 | Destroys the Swedish cup by freeing its entrant list, round table, tie arrays, stats, club pool and stage objects, then runs the Cup destructor. | high | opus |  |
| 0x88cf40 | 424 | `SweCup::create_round_table` | thiscall(SweCup* this, char stage, short* round_count, short* name_base, int* flag) ret 0x10 | Builds the two-round table of a preliminary section for stages below 7, or the six-round main draw table of 64 clubs for stage 7. | high | opus |  |
| 0x88d5a0 | 68 | `SweCup::collect_entrants` | thiscall(SweCup* this) ret 0 | Fills the 30-entry six-byte entrant list at +0xa7 with the first 30 clubs of the club pool and clears those pool slots. | medium | opus |  |
| 0x88d690 | 158 | `SweCup::start_new_season` | thiscall(SweCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds the club pool, entrants, rounds, fixture tree, preliminary stages and ranking. | high | opus |  |
| 0x88d8a0 | 41 | `SweCup::update_for_date` | thiscall(SweCup* this, Date* today, int phase) ret 8 | Starts a new cup season on day 1 of month index 6 when the cup is complete, then runs the Cup daily update. | high | opus |  |
| 0x88d910 | 93 | `SweCup::build_fate_news_text` | thiscall(SweCup* this, int club_index, char fate, char stage, ..., int full_result, ...) ret 0x28 | Writes news that a club goes through to the Swedish Cup Third Round from a preliminary stage, and defers other fates to the Comp base. | high | opus |  |
| 0x88da20 | 269 | `SweCup::build_club_pool` | thiscall(SweCup* this) ret 0 | Collects 244 Swedish clubs from four divisions into the pool at +0xb2 and deals them into eight sections with random seeded clubs. | high | sonnet |  |
| 0x88dda0 | 168 (+1 unwind) | `SweCup::create_preliminary_stage` | thiscall(SweCup* this, char stage) ret 4 | Takes the next 31 or 30 clubs from the pool and builds the Cup_Stage of that preliminary section in the stage slot. | high | opus |  |
| 0x88dfd0 | 40 | `SweCup::advance_stage` | thiscall(SweCup* this) ret 0 | Moves to the next stage, asserting at the last stage, and builds the 64-club main draw when the stage reaches 7. | high | opus |  |
| 0x88e060 | 199 (+1 unwind) | `SweCup::create_main_draw_stage` | thiscall(SweCup* this) ret 0 | Collects the 64 qualified clubs from the base entrant list and the seven preliminary stages and builds and draws the stage 7 Cup_Stage. | high | opus |  |
| 0x88e2f0 | 108 | `SweCup::update_staff_records_for_status` | thiscall(SweCup* this, Club* club, char outcome, char stage, int arg4, Fixture* fixture, int arg6) ret 0x18 | Adds a staff history record when a club goes out or through in a preliminary stage, or wins or loses the main draw final. | high | opus |  |
| 0x88e420 | 105 | `SweCup::rank_teams` | thiscall(SweCup* this) ret 0 | Sorts the club pool and gives each club a final position in Comp_Stats from the round in which it went out. | high | opus |  |
| 0x88e580 | 29 | `SweCup::set_club_progress` | stdcall(Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Writes a club's three progress codes in its Comp_Stats entry, scaling them by eight for preliminary stages below 7. | high | opus |  |
