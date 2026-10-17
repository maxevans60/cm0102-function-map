# asia_super_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x410650 | 131 (+2 unwind) | `AsiaSuperCup::AsiaSuperCup` | thiscall(AsiaSuperCup* this, short year, Comp* owner) ret 8, returns this | Constructs the Asian Super Cup on the Cup base and, when no saved data loads, picks its two clubs and sets up its single round. | high | opus | club-world.md |
| 0x410820 | 11 | `AsiaSuperCup::`scalar deleting destructor'` | thiscall(AsiaSuperCup* this, unsigned flags) ret 4, returns this | Runs the Asian Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x410840 | 62 (+1 unwind) | `AsiaSuperCup::~AsiaSuperCup` | thiscall(AsiaSuperCup* this) ret 0 | Destroys the Asian Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x410910 | 98 | `AsiaSuperCup::create_round_table` | thiscall(AsiaSuperCup* this, char stage, short* round_count, short* schedule_id, int* is_league) ret 0x10, returns table or null | Builds the one-round table of the Asian Super Cup with its draw and match dates for two teams. | high | opus | 2026-10-16-sweep-europe.md |
| 0x410a50 | 148 | `AsiaSuperCup::select_teams` | thiscall(AsiaSuperCup* this) ret 0, returns 1, 0 or -1 | Picks the Asian Club Championship winner and the Asian Cup Winners' Cup winner, or the runner-up when one club won both. | high | opus | 2026-10-16-sweep-europe.md |
| 0x410c50 | 139 | `AsiaSuperCup::start_new_season` | thiscall(AsiaSuperCup* this) ret 0 | In month 5 clears the finished Asian Super Cup, archives its stats, moves the year on and sets up the next edition. | high | opus |  |
| 0x410e20 | 41 | `AsiaSuperCup::update_for_date` | thiscall(AsiaSuperCup* this, Date* today, int full_update) ret 8 | On day 25 of month 5, after the cup ends, starts the next edition through release_data, then runs the Cup daily update. | high | opus |  |
