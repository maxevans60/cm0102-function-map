# fra_first.cpp: 14 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5bb160 | 292 (+6 unwind) | `FraFirst::FraFirst` | thiscall(FraFirst* this, short season_year, int comp_record) ret 8, returns this | Constructs the French First Division, creates placeholder comps for CFA and the lower division, then loads saved data or builds rules, table, fixtures and stats. | high | opus | fra.md |
| 0x5bb540 | 2 | `stub_return_one_ret8` | thiscall(Comp* this, int a, int b) ret 8, returns 1 | Shared stub that ignores its two arguments and returns one, used as add_result of competitions that never play matches. | high | opus |  |
| 0x5bb550 | 2 | `stub_return_one_ret4` | thiscall(void* this, int a) ret 4, returns 1 | Shared stub that ignores its argument and returns one, the default for Comp slot 25 and RulingBody slot 6. | high | opus |  |
| 0x5bb560 | 11 | `FraCfaStubComp::`scalar deleting destructor'` | thiscall(FraCfaStubComp* this, unsigned flags) ret 4, returns this | Runs the destructor of the CFA placeholder comp and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bb580 | 2 | `FraCfaStubComp::~FraCfaStubComp` | thiscall(FraCfaStubComp* this) ret 0 | Restores the CFA placeholder vtable and runs the Comp destructor. | high | opus |  |
| 0x5bb590 | 11 | `FraLowerStubComp::`scalar deleting destructor'` | thiscall(FraLowerStubComp* this, unsigned flags) ret 4, returns this | Runs the destructor of the French lower division placeholder comp and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bb5b0 | 2 | `FraLowerStubComp::~FraLowerStubComp` | thiscall(FraLowerStubComp* this) ret 0 | Restores the lower division placeholder vtable and runs the Comp destructor. | high | opus |  |
| 0x5bb5c0 | 11 | `FraFirst::`scalar deleting destructor'` | thiscall(FraFirst* this, unsigned flags) ret 4, returns this | Runs the FraFirst destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bb5e0 | 50 (+1 unwind) | `FraFirst::~FraFirst` | thiscall(FraFirst* this) ret 0 | Destroys the French First Division, freeing its table, schedule, stats and both placeholder comps before the League destructor. | high | opus |  |
| 0x5bb690 | 1331 | `FraFirst::create_schedule` | thiscall(FraFirst* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the league schedule for stage -1, with 34 rounds in 2001 and 38 rounds later, and returns null for any other stage. | high | opus |  |
| 0x5bc2b0 | 109 | `FraFirst::create_table` | thiscall(FraFirst* this) ret 0, returns 1 on success and 0 on failure | Allocates the table with 18 rows in 2001 and 20 later, fills it with First Division clubs, sets the prize fund and pays the clubs. | high | opus |  |
| 0x5bc410 | 43 | `FraFirst::set_up_rules` | thiscall(FraFirst* this) ret 0, returns 1 | Sets the First Division rule bytes, with no division above and the Second Division below, and builds the schedule through slot 15. | high | opus |  |
| 0x5bc4d0 | 202 (+2 unwind) | `FraFirst::start_new_season` | thiscall(FraFirst* this) ret 0 | Runs promotion and relegation, swaps clubs between CFA and National, rebuilds the table and fixtures, and starts the Second Division and National seasons. | high | opus |  |
| 0x5bc780 | 172 | `FraFirst::exchange_cfa_national_clubs` | thiscall(FraFirst* this) ret 0 | Promotes the top CFA clubs into National, six in 2001 and four later, and moves relegated National clubs back to the CFA. | high | opus |  |
