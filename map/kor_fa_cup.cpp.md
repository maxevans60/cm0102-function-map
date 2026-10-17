# kor_fa_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x66a460 | 130 (+2 unwind) | `KorFaCup::KorFaCup` | thiscall(KorFaCup* this, short year, void* comp_record) ret 8, returns this | Constructs the Korean FA Cup on Cup, loads it from disk or collects entrants and builds the round table, fixture tree, stats and ranking. | high | opus |  |
| 0x66a630 | 11 | `KorFaCup::`scalar deleting destructor'` | thiscall(KorFaCup* this, unsigned flags) ret 4, returns this | Runs the Korean FA Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x66a650 | 62 (+1 unwind) | `KorFaCup::~KorFaCup` | thiscall(KorFaCup* this) ret 0 | Destroys the Korean FA Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x66a720 | 250 | `KorFaCup::create_round_table` | thiscall(KorFaCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Allocates and fills the five-round table of the Korean FA Cup with draw dates, match dates and round rules for the current year. | high | opus |  |
| 0x66aaf0 | 140 | `KorFaCup::collect_entrants` | thiscall(KorFaCup* this) ret 0, returns 1 when 32 entries fill, 0 when short, -1 on allocation failure | Fills the 32-entry entrant list with 22 top Korean clubs from outside the K League, then adds the K League clubs. | high | opus |  |
| 0x66acc0 | 132 | `KorFaCup::start_new_season` | thiscall(KorFaCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rounds, fixture tree and ranking. | high | opus |  |
