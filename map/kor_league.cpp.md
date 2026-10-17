# kor_league.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x66ae70 | 156 (+2 unwind) | `KorLeague::KorLeague` | thiscall(KorLeague* this, short comp_id, Division* division) returning this, ret 8 | Constructs the Korean league on the League base, loads saved state or sets rules, builds the ten-club table, fixtures and Comp_Stats. | high | opus |  |
| 0x66b080 | 11 | `KorLeague::`scalar deleting destructor'` | thiscall(KorLeague* this, unsigned flags) returning this, ret 4 | Runs the Korean league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x66b0a0 | 38 (+1 unwind) | `KorLeague::~KorLeague` | thiscall(KorLeague* this), ret 0 | Destroys the Korean league, freeing its table, its schedule at +0xba and its Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x66b130 | 1120 | `KorLeague::create_schedule` | thiscall(KorLeague* this, char stage, short* round_count, short* stage_id, int* is_league) returning schedule pointer, ret 0x10 | Builds the 27-round match date template of the Korean league season, with a later start date in the 2002 season. | high | opus |  |
| 0x66bba0 | 92 | `KorLeague::create_table` | thiscall(KorLeague* this), returns int 1 on success or 0, ret 0 | Allocates the league table and fills it with the ten clubs whose division is this league, then sets the prize fund. | high | opus |  |
| 0x66bcc0 | 37 | `KorLeague::set_up_rules` | thiscall(KorLeague* this), returns int 1, ret 0 | Sets the Korean league rule bytes, points values and tiebreak list, then builds the season schedule through create_schedule. | high | opus |  |
| 0x66bd60 | 128 | `KorLeague::start_new_season` | thiscall(KorLeague* this), ret 0 | Resets the Korean league for a new season, archives statistics, rebuilds rules, table and fixtures, and renews officials. | high | opus |  |
