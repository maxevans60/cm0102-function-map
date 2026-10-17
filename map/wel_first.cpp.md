# wel_first.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x924e30 | 156 (+2 unwind) | `WelFirst::WelFirst` | thiscall(WelFirst* this, short comp_id, CompRecord* comp) ret 8, returns this | Constructs the League of Wales on League, then loads saved data or sets rules, builds the 18-club table, fixtures and Comp_Stats. | high | opus |  |
| 0x925040 | 11 | `WelFirst::`scalar deleting destructor'` | thiscall(WelFirst* this, unsigned flags) ret 4, returns this | Runs the WelFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x925060 | 38 (+1 unwind) | `WelFirst::~WelFirst` | thiscall(WelFirst* this) ret 0 | Destroys the League of Wales, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x9250f0 | 1063 | `WelFirst::create_schedule` | thiscall(WelFirst* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 34-round League of Wales schedule from mid August, with the last rounds placed by the weekday of a set date. | high | opus |  |
| 0x925b30 | 94 | `WelFirst::create_table` | thiscall(WelFirst* this) ret 0, returns 1 on success and 0 on failure | Allocates the 18-row table, fills it with the clubs of the Welsh league division and sets a prize fund of 10000. | high | opus | 2026-10-16-research-name-check.md, wal-nir-irl.md |
| 0x925c50 | 40 | `WelFirst::set_up_rules` | thiscall(WelFirst* this) ret 0, returns 1 | Sets the League of Wales rule bytes, with no upper or lower league, and builds the season schedule. | high | opus |  |
| 0x925cf0 | 128 | `WelFirst::start_new_season` | thiscall(WelFirst* this) ret 0 | Frees last season's table and schedule, archives stats, advances the year and rebuilds rules, table, fixtures and predicted positions. | high | opus |  |
