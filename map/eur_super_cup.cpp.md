# eur_super_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x57a100 | 133 (+2 unwind) | `EurSuperCup::EurSuperCup` | thiscall(EurSuperCup* this, short year, Comp* owner) ret 8, returns this | Constructs the European Super Cup on the Cup base and, when no saved data loads, picks its two clubs, builds its round table and stats. | high | opus |  |
| 0x57a2d0 | 11 | `EurSuperCup::`scalar deleting destructor'` | thiscall(EurSuperCup* this, unsigned flags) ret 4, returns this | Runs the European Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x57a2f0 | 62 (+1 unwind) | `EurSuperCup::~EurSuperCup` | thiscall(EurSuperCup* this) ret 0 | Destroys the European Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x57a3c0 | 98 | `EurSuperCup::create_round_table` | thiscall(EurSuperCup* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10, returns table or null | Builds the one-round table of the European Super Cup with its draw and match dates for two teams. | high | opus | 2026-10-16-sweep-europe.md |
| 0x57a500 | 134 | `EurSuperCup::select_teams` | thiscall(EurSuperCup* this) ret 0, returns 1, 0 or -1 | Picks the two Super Cup clubs as the latest winners of two European club competitions, with a different second competition in 1999. | high | opus | 2026-10-16-sweep-europe.md |
| 0x57a6d0 | 135 | `EurSuperCup::start_new_season` | thiscall(EurSuperCup* this) ret 0 | Clears the finished European Super Cup, archives its stats, moves the year on and picks the clubs and round of the next edition. | high | opus |  |
