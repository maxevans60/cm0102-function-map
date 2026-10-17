# kor_super_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x66d820 | 128 (+2 unwind) | `KorSuperCup::KorSuperCup` | thiscall(KorSuperCup* this, short comp_id, Division* division) returning this, ret 8 | Constructs the Korean Super Cup on the Cup base, loads saved state or picks its two clubs and builds the round table and fixture tree. | high | opus |  |
| 0x66d9e0 | 11 | `KorSuperCup::`scalar deleting destructor'` | thiscall(KorSuperCup* this, unsigned flags) returning this, ret 4 | Runs the Korean Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x66da00 | 62 (+1 unwind) | `KorSuperCup::~KorSuperCup` | thiscall(KorSuperCup* this), ret 0 | Destroys the Korean Super Cup, freeing its team record, round table, fixture tree and Comp_Stats, then runs the Cup destructor. | high | opus |  |
| 0x66dad0 | 99 | `KorSuperCup::create_round_table` | thiscall(KorSuperCup* this, char stage, short* round_count, short* stage_id, int* is_league) returning round table pointer, ret 0x10 | Builds the single round of the Korean Super Cup, a one-match final between two clubs. | high | opus |  |
| 0x66dc10 | 188 | `KorSuperCup::create_table` | thiscall(KorSuperCup* this), returns int 1, 0 on failure or -1 on allocation failure, ret 0 | Picks the two Super Cup clubs, the Korean League champion and the Korean FA Cup winner, with fallbacks to a runner-up or a club of the nation. | high | sonnet |  |
| 0x66de90 | 125 | `KorSuperCup::start_new_season` | thiscall(KorSuperCup* this), ret 0 | Resets the Super Cup for a new season, frees old tables, archives statistics, picks the two clubs again and rebuilds the rounds. | high | opus |  |
