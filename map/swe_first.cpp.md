# swe_first.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x88e5e0 | 159 (+2 unwind) | `SweFirst::SweFirst` | thiscall(SweFirst* this, short year, Nation* nation) ret 8 | Constructs the Swedish First Division on League, then loads it or sets up the rules, 16-club table, fixtures, sort and Comp_Stats object. | high | opus |  |
| 0x88e800 | 11 | `SweFirst::`scalar deleting destructor'` | thiscall(SweFirst* this, unsigned flags) ret 4 | Runs the SweFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x88e820 | 57 (+1 unwind) | `SweFirst::~SweFirst` | thiscall(SweFirst* this) ret 0 | Frees the table, the base schedule, every stage object and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x88e8e0 | 735 | `SweFirst::create_schedule` | thiscall(SweFirst* this, char stage, short* round_count, short* name_base, int* flag) ret 0x10 | Builds the round dates of the 30-round league for stage -1, or the one-round two-legged play-off template for stage 0. | high | opus |  |
| 0x88ef90 | 84 | `SweFirst::create_table` | thiscall(SweFirst* this) ret 0 | Allocates the 16-row table and fills it with the clubs of the Swedish First Division. | high | opus |  |
| 0x88f090 | 50 | `SweFirst::set_up_rules` | thiscall(SweFirst* this) ret 0 | Sets the league rules of the Swedish First Division, with promotion to the Premier Division, and builds the base league schedule. | high | opus |  |
| 0x88f150 | 143 | `SweFirst::start_new_season` | thiscall(SweFirst* this) ret 0 | Archives the season, deletes the old stages and rebuilds the rules, table, fixtures and predicted positions for the new season. | high | opus |  |
| 0x88f310 | 59 | `SweFirst::advance_stage` | thiscall(SweFirst* this) ret 0 | Moves to the next stage once the Premier Division is complete, and builds the promotion play-off at stage 0. | high | opus |  |
| 0x88f3e0 | 174 (+1 unwind) | `SweFirst::create_play_off_stage` | thiscall(SweFirst* this) ret 0 | Builds stage 0, a two-club tie between the First Division club with play-off status and the Premier Division play-off club. | high | opus |  |
| 0x88f600 | 182 | `SweFirst::update_staff_records_for_status` | thiscall(SweFirst* this, Club* club, char status, char stage, ...) ret 0x18 | Adds staff history records for champions, promoted and relegated clubs, and sets table status bytes for the play-off winner and loser. | high | opus |  |
| 0x88f7f0 | 187 | `SweFirst::build_fate_news_text` | stdcall(int club_index, char fate, char stage, ..., int comp_id, ..., int full_result, ...) ret 0x28 | Writes news that a club avoids relegation, wins promotion or goes down after the play-off, and defers other fates to the Comp base. | high | opus |  |
| 0x88fa10 | 88 | `SweFirst::set_club_progress` | stdcall(Club* club, char stage, char code1, char code2, char code3) ret 0x14 | Writes a club's three progress codes in its Comp_Stats entry, mapping play-off results to codes 10 and 13 for Premier Division clubs. | high | opus |  |
