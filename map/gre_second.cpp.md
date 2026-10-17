# gre_second.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5eb2b0 | 156 (+2 unwind) | `GreSecond::GreSecond` | thiscall(GreSecond* this, short year, void* comp_record) ret 8, returns this | Constructs the Greek Second Division on League, loads it from the temp file or sets rules, fills the table, makes fixtures and creates Comp_Stats. | high | opus |  |
| 0x5eb4c0 | 11 | `GreSecond::`scalar deleting destructor'` | thiscall(GreSecond* this, unsigned flags) ret 4, returns this | Runs the GreSecond destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5eb4e0 | 38 (+1 unwind) | `GreSecond::~GreSecond` | thiscall(GreSecond* this) ret 0 | Destroys the Greek Second Division, freeing its table, schedule and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x5eb570 | 751 | `GreSecond::create_schedule` | thiscall(GreSecond* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 30-round season schedule of the Greek Second Division from September to April, or a three-round stage 0 schedule in May. | high | opus |  |
| 0x5ebcb0 | 99 | `GreSecond::create_table` | thiscall(GreSecond* this) ret 0, returns 1 on success and 0 on failure | Allocates the 14-row table, fills it with the clubs of the Greek Second Division, sets the prize fund and pays each club 500000. | high | opus |  |
| 0x5ebde0 | 44 | `GreSecond::set_up_rules` | thiscall(GreSecond* this) ret 0, returns 1 | Sets the Greek Second Division rule bytes with the First Division above and no division below, then builds the schedule through create_schedule. | high | opus |  |
| 0x5ebe90 | 134 | `GreSecond::start_new_season` | thiscall(GreSecond* this) ret 0 | Frees the old table and schedule, archives Comp_Stats, increments the year and rebuilds rules, table, fixtures and order. | high | opus |  |
