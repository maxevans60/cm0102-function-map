# eng_third.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x576dd0 | 161 (+2 unwind) | `EngThird::EngThird` | thiscall(EngThird* this, short year, club_comp* comp) ret 8, returns this | Constructs the English Third Division on the League base, loads it from the temp file or sets up its rules, table, fixtures and stats. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x577000 | 11 | `EngThird::`scalar deleting destructor'` | thiscall(EngThird* this, unsigned flags) ret 4, returns this | Runs the Third Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x577020 | 60 (+1 unwind) | `EngThird::~EngThird` | thiscall(EngThird* this) ret 0 | Destroys the Third Division by freeing its table, schedule, stage objects and stats, then runs the League destructor. | high | opus |  |
| 0x5770e0 | 1607 | `EngThird::create_schedule` | thiscall(EngThird* this, char stage, short* round_count, short* out2, int* is_league) ret 0x10, returns schedule pointer | Builds the 46-matchday league schedule for stage -1 or the two-round play-off table for stage 0, with dates in the season year. | high | opus |  |
| 0x577f70 | 103 | `EngThird::create_table` | thiscall(EngThird* this) ret 0, returns 1 on success | Allocates the 24-row league table, fills it with the Third Division clubs, sets the prize fund and pays the clubs. | high | opus |  |
| 0x5780c0 | 48 | `EngThird::set_up_rules` | thiscall(EngThird* this) ret 0, returns 1 | Sets the Third Division rules with three promoted clubs and four play-off places, relegating one club to the Conference when it exists. | high | opus |  |
| 0x578170 | 143 | `EngThird::start_new_season` | thiscall(EngThird* this) ret 0 | Clears the old season, archives the stats, moves the year on and rebuilds the rules, table, fixtures and predicted positions. | high | opus |  |
| 0x578330 | 40 | `EngThird::advance_stage` | thiscall(EngThird* this) ret 0 | Moves the division to its next stage and builds the play-off stage when stage 0 starts, or reports an error after the last stage. | high | opus |  |
| 0x5783c0 | 138 (+1 unwind) | `EngThird::create_play_off_stage` | thiscall(EngThird* this) ret 0 | Takes the clubs in fourth to seventh place, builds the four-club play-off Cup_Stage and sets up its first round. | high | opus |  |
| 0x5785b0 | 61 | `EngThird::build_fate_news_text` | thiscall(EngThird* this, int club_index, char fate, char flag, int a4, int a5, int a6, int a7, int a8, int full_sentence, int a10) ret 0x28 | Writes the short headline that a club wins promotion for play-off winners, or passes other fates to the Comp base builder. | high | opus |  |
| 0x578660 | 102 | `EngThird::set_club_progress` | thiscall(EngThird* this, Club* club, char stage, char code_73, char code_74, char code_75) ret 0x14 | Stores the three progress bytes of a club's stats entry, mapping play-off codes 1 to 3 onto 4 to 6. | medium | opus |  |
