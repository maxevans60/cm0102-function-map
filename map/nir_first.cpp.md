# nir_first.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x78b010 | 159 (+2 unwind) | `NirFirst::NirFirst` | thiscall(NirFirst* this, short year, int nation), ret 8 | Constructs the Northern Irish First Division on the League base and, when no saved data loads, sets its rules, table, fixtures and Comp_Stats object. | high | opus |  |
| 0x78b230 | 11 | `NirFirst::`scalar deleting destructor'` | thiscall(NirFirst* this, unsigned flags), ret 4 | Destroys the Northern Irish First Division and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x78b250 | 60 (+1 unwind) | `NirFirst::~NirFirst` | thiscall(NirFirst* this), ret 0 | Restores the league vtable, frees the table, schedule and stage objects and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x78b310 | 1024 | `NirFirst::create_schedule` | thiscall(NirFirst* this, char stage, short* round_count, short* extra, int* is_league), ret 0x10 | Builds the 36-matchday league schedule for stage -1, or the one two-legged play-off round for stage 0. | high | opus |  |
| 0x78bc50 | 95 | `NirFirst::create_table` | thiscall(NirFirst* this) ret 0, returns 1, or 0 on failure | Allocates the ten-row table, fills it with the clubs of the Northern Irish First Division and sets the prize fund. | high | opus |  |
| 0x78bd70 | 42 | `NirFirst::set_up_rules` | thiscall(NirFirst* this) ret 0, returns 1 | Sets the First Division rule bytes, four meetings a season and the Premier Division as the division above, then builds the schedule. | high | opus |  |
| 0x78be10 | 143 | `NirFirst::start_new_season` | thiscall(NirFirst* this), ret 0 | Frees last season's table, schedule and play-off stage, archives the stats, moves the year on and rebuilds the rules, table and fixtures. | high | opus |  |
| 0x78bfd0 | 59 | `NirFirst::advance_stage` | thiscall(NirFirst* this), ret 0 | Once the Premier Division is complete, moves the stage counter on and builds the promotion play-off stage when stage 0 starts. | high | opus |  |
| 0x78c0a0 | 191 (+1 unwind) | `NirFirst::create_playoff_stage` | thiscall(NirFirst* this), ret 0 | Builds the two-club promotion play-off between the First Division club with play-off status and the Premier Division club with relegation play-off status. | high | opus |  |
| 0x78c300 | 181 | `NirFirst::update_staff_records_for_status` | thiscall(NirFirst* this, Club* club, char status, char stage, int a4, int a5, int a6), ret 0x18 | Writes staff records for First Division titles, play-off places and relegation, and settles promotion or relegation for both play-off clubs. | high | opus |  |
| 0x78c4f0 | 136 | `NirFirst::build_fate_news_text` | thiscall(NirFirst* this, int club_index, char fate, char stage, int a4, int a5, int a6, int comp_key, int a8, int full_sentence, int a10), ret 0x28 | Writes the play-off news that a club avoids relegation, wins promotion or goes down, and uses the base fate text otherwise. | high | opus |  |
| 0x78c670 | 98 | `NirFirst::set_club_progress` | thiscall(NirFirst* this, Club* club, char stage, char code_73, char code_74, char code_75), ret 0x14 | Maps league and play-off progress codes to final position codes and writes the three progress bytes of a club's statistics entry. | high | opus |  |
