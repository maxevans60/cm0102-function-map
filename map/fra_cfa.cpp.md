# fra_cfa.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5b91c0 | 175 (+1 unwind) | `FraCfa::FraCfa` | thiscall(FraCfa* this, short season_year) ret 4, returns this | Constructs the French CFA background league, collects and shuffles up to 72 clubs, and builds a table and fixtures for four groups of 18. | high | opus | fra.md |
| 0x5b9420 | 2 | `stub_return_zero_ret8` | thiscall(Comp* this, int a, int b) ret 8, returns false in AL | Shared stub that ignores its two arguments and returns false, used as check_complete and update_for_date of competitions that never run. | high | opus |  |
| 0x5b9430 | 2 | `stub_return_zero_ret4` | thiscall(Comp* this, int a) ret 4, returns 0 | Shared stub that ignores its argument and returns zero, so a competition refuses league fixtures and fills unused slots 32 and 33. | high | opus |  |
| 0x5b9440 | 11 | `FraCfa::`scalar deleting destructor'` | thiscall(FraCfa* this, unsigned flags) ret 4, returns this | Runs the FraCfa destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5b9460 | 52 (+1 unwind) | `FraCfa::~FraCfa` | thiscall(FraCfa* this) ret 0 | Destroys the French CFA league by freeing its table, schedule and stage objects, then runs the League destructor. | high | opus |  |
| 0x5b9510 | 1149 | `FraCfa::create_schedule` | thiscall(FraCfa* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 34-round schedule of one 18-club CFA group for stage -1 and returns null for any other stage. | high | opus |  |
| 0x5b9fa0 | 85 | `FraCfa::create_group_table` | thiscall(FraCfa* this, Club** clubs) ret 4, returns 1 when all 18 rows fill | Allocates the 18-row table of one CFA group and adds each club of the given array, flagging clubs of the top two divisions. | medium | opus |  |
| 0x5ba0a0 | 33 | `FraCfa::set_up_rules` | thiscall(FraCfa* this) ret 0, returns 1 | Sets the CFA league rule bytes, with no division below, and builds the season schedule through slot 15. | high | opus |  |
