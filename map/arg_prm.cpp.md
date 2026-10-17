# arg_prm.cpp: 17 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x404250 | 164 (+2 unwind) | `ArgPrm::ArgPrm` | thiscall(ArgPrm* this, short year, CompRecord* comp), ret 8 | Constructs the Argentine Premier Division on League, then loads saved data or sets up rules, table, fixtures, stats, both stages and the relegation averages. | high | opus |  |
| 0x404480 | 2 | `shared_return_true` | thiscall(Comp* this), returns 1, ret 0 | Returns 1 as a shared override of three different competition vtable slots. | high | opus |  |
| 0x404490 | 11 | `ArgPrm::`scalar deleting destructor'` | thiscall(ArgPrm* this, unsigned flags), returns this, ret 4 | Destroys the Argentine Premier Division object and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x4044b0 | 58 (+1 unwind) | `ArgPrm::~ArgPrm` | thiscall(ArgPrm* this), ret 0 | Destroys the Argentine Premier Division, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x404570 | 1686 | `ArgPrm::create_schedule` | thiscall(ArgPrm* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 19-round schedule template of the first half from August for stage -1, or the second half from late January for stage 0. | high | opus |  |
| 0x405540 | 99 | `ArgPrm::create_table` | thiscall(ArgPrm* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 20-row table, fills it with the clubs of the Argentine Premier Division, sets the prize fund and pays each club 500000. | high | opus |  |
| 0x405670 | 45 | `ArgPrm::set_up_rules` | thiscall(ArgPrm* this), returns int, ret 0 | Sets the Argentine league rules, with the Second Division as the lower league, and builds the schedule for stage -1. | high | opus |  |
| 0x405720 | 181 | `ArgPrm::start_new_season` | thiscall(ArgPrm* this), ret 0 | Rolls the relegation averages, promotes and relegates clubs, clears the old season and rebuilds rules, table, fixtures and stages for the new year. | high | opus |  |
| 0x405950 | 238 (+2 unwind) | `ArgPrm::create_stages` | thiscall(ArgPrm* this), ret 0 | Creates the two half-season League_Stage objects of the Argentine Premier Division from the schedules of stages 0 and 1. | medium | opus |  |
| 0x405c50 | 28 | `ArgPrm::add_result` | thiscall(ArgPrm* this, Fixture* match, int update_stats), returns 1, ret 8 | Adds a match to the table and its stage, then adds it again with stats off and the fixture flag at +0x42 set. | high | opus |  |
| 0x405ca0 | 191 | `ArgPrm::record_season_honours` | thiscall(ArgPrm* this), ret 0 | Relegates the two clubs with the lowest points average, marks them in the table and both stages, then stores the season honours. | high | opus |  |
| 0x405ef0 | 410 | `ArgPrm::init_relegation_averages` | thiscall(ArgPrm* this), ret 0 | Allocates the 0x13-byte relegation average rows and seeds them with fixed points from two earlier 38-match seasons for named clubs. | high | opus |  |
| 0x406570 | 206 | `ArgPrm::update_relegation_averages` | thiscall(ArgPrm* this, int new_season), ret 4 | Copies season points and matches into the relegation average rows, works out each three-season average and sorts the rows, rolling seasons when asked. | high | opus |  |
| 0x4067f0 | 79 | `ArgPrm::process_promotion_relegation_chain` | thiscall(ArgPrm* this, int pairwise unused), ret 4 | Records final positions in both divisions, promotes the Second Division clubs with status 0 or 5 and moves relegated Premier clubs down. | high | opus |  |
| 0x4068d0 | 162 | `arg_prm_swap_second_and_third_division_clubs` | cdecl, no arguments, ret 0 | Moves up to four relegated Second Division clubs to the Argentine Third Division and promotes the same number of top Third Division clubs. | high | opus |  |
| 0x406aa0 | 78 | `ArgPrm::build_fate_news_text` | thiscall(ArgPrm* this, int club_index, char fate, char stage, ..., int full_sentence, ...), ret 0x28 | Writes the news that a club is relegated from the Argentine Premier Division for its poor average, else uses the base fate text. | high | opus |  |
| 0x406b80 | 38 | `ArgPrm::set_club_progress` | thiscall(ArgPrm* this, Club* club, char stage, char code1, char code2, char code3), ret 0x14 | Stores the three progress codes of a club in its Comp_Stats entry, capping codes above 17 at 18 for stages -1, 0 and 1. | high | opus |  |
