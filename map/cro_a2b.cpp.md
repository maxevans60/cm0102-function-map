# cro_a2b.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x516430 | 158 (+2 unwind) | `CroA2b::CroA2b` | thiscall(CroA2b* this, short season_year, int parent) ret 8 | Constructs this Croatian second division on League, loads it from the temp file or sets rules, table, fixtures and Comp_Stats. | high | opus |  |
| 0x516650 | 11 | `CroA2b::`scalar deleting destructor'` | thiscall(CroA2b* this, unsigned flags) ret 4 | Runs the CroA2b destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x516670 | 38 (+1 unwind) | `CroA2b::~CroA2b` | thiscall(CroA2b* this) ret 0 | Destroys this Croatian second division by freeing its table, its schedule at +0xba and its Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x516700 | 739 | `CroA2b::create_schedule` | thiscall(CroA2b* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10 | Builds the 30-round season template for stage -1 or a one-round tie-break play-off template sized from the tie count at +0xee for stage 0. | high | opus |  |
| 0x516dd0 | 99 | `CroA2b::create_table` | thiscall(CroA2b* this) ret 0, returns 1 on success or 0 | Allocates the 16-row table, fills it with the clubs of comp id 0x9cf8ac, then sets the prize fund and pays each club. | high | opus |  |
| 0x516f00 | 46 | `CroA2b::set_up_rules` | thiscall(CroA2b* this) ret 0, returns 1 | Sets the rule bytes and linked comp ids of this Croatian second division, then builds the season schedule through create_schedule. | high | opus |  |
| 0x516fc0 | 135 | `CroA2b::start_new_season` | thiscall(CroA2b* this) ret 0 | Frees the old table, schedule and play-off data, archives Comp_Stats, increments the year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
| 0x517180 | 40 | `CroA2b::advance_stage` | thiscall(CroA2b* this) ret 0 | Moves the current stage index on by one and builds the tie-break play-off stage when the index reaches stage 0. | high | opus |  |
| 0x517210 | 192 (+1 unwind) | `CroA2b::create_tiebreak_playoff_stage` | thiscall(CroA2b* this) ret 0 | Pairs adjacent table rows level on the row value at +0x19 into play-off ties and builds their Cup_Stage, or ends the season. | medium | opus |  |
