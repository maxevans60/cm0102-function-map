# tur_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8fc3b0 | 132 (+2 unwind) | `TurCup::TurCup` | thiscall(TurCup* this, short season, int nation), ret 8 | Constructs the Turkish Cup, loads it from disk or collects its 64 entrants, builds the round table and fixture tree and its stats. | high | opus |  |
| 0x8fc580 | 11 | `TurCup::`scalar deleting destructor'` | thiscall(TurCup* this, unsigned flags), ret 4 | Destroys the Turkish Cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x8fc5a0 | 62 (+1 unwind) | `TurCup::~TurCup` | thiscall(TurCup* this), ret 0 | Restores the Turkish Cup vtable, frees the entrant list, round table and tie arrays, deletes the stats and runs the Cup destructor. | high | opus |  |
| 0x8fc670 | 324 | `TurCup::create_round_table` | thiscall(TurCup* this, char stage, short* round_count, short* extra, int* out), ret 0x10 | Builds the seven-round Turkish Cup table with draw and match dates for each round of the season. | high | opus |  |
| 0x8fcb90 | 159 | `TurCup::collect_entrants` | thiscall(TurCup* this), returns 1 or -1 on allocation failure, ret 0 | Fills the 64-entry six-byte entrant list with Turkish clubs, premier clubs at the end and the lower two divisions sorted into early rounds. | high | opus |  |
| 0x8fcdb0 | 132 | `TurCup::start_new_season` | thiscall(TurCup* this), ret 0 | Frees last season's cup data, archives the stats, advances the season and rebuilds the entrants, rounds and fixture tree. | high | opus | 2026-10-16-research-name-check.md |
