# tur_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8fe6f0 | 156 (+2 unwind) | `TurSecond::TurSecond` | thiscall(TurSecond* this, short season, int nation), ret 8 | Constructs the Turkish second division, loads it from the temp file or sets its rules, table, fixtures and stats. | high | opus |  |
| 0x8fe900 | 11 | `TurSecond::`scalar deleting destructor'` | thiscall(TurSecond* this, unsigned flags), ret 4 | Destroys the Turkish second division and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x8fe920 | 38 (+1 unwind) | `TurSecond::~TurSecond` | thiscall(TurSecond* this), ret 0 | Restores the Turkish second division vtable, frees its table and schedule, deletes the stats and runs the League destructor. | high | opus |  |
| 0x8fe9b0 | 816 | `TurSecond::create_schedule` | thiscall(TurSecond* this, char stage, short* round_count, short* extra, int* out), ret 0x10 | Builds the 38-round Turkish second division schedule with a date and match slots for each round. | high | opus |  |
| 0x8ff150 | 95 | `TurSecond::create_table` | thiscall(TurSecond* this), returns 1 on success and 0 on failure, ret 0 | Allocates the 20-row table, fills it with the clubs of the Turkish second division and pays each club 100000. | high | opus |  |
| 0x8ff280 | 42 | `TurSecond::set_up_rules` | thiscall(TurSecond* this), returns 1, ret 0 | Sets the Turkish second division rules, linking the premier division above and the third tier below, and builds its schedule. | high | opus |  |
| 0x8ff330 | 125 | `TurSecond::start_new_season` | thiscall(TurSecond* this), ret 0 | Frees last season's table and schedule, archives the stats and rebuilds the rules, table and fixtures for the new season. | high | opus |  |
