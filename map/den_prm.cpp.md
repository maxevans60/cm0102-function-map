# den_prm.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5525e0 | 187 (+2 unwind) | `DenPrm::DenPrm` | thiscall(DenPrm* this, short year, CompRecord* comp) ret 8, returns this | Constructs the Danish Premier Division on League, moves Kvalifikationsraekken clubs to the lower division, then loads or builds rules, table and fixtures. | high | opus |  |
| 0x552850 | 11 | `DenPrm::`scalar deleting destructor'` | thiscall(DenPrm* this, unsigned flags) ret 4, returns this | Runs the Danish Premier Division destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x552870 | 38 (+1 unwind) | `DenPrm::~DenPrm` | thiscall(DenPrm* this) ret 0 | Destroys the Danish Premier Division, freeing its table, schedule and stats before the League destructor runs. | high | opus |  |
| 0x552900 | 1731 | `DenPrm::create_schedule` | thiscall(DenPrm* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 33-round schedule template of the Danish Premier Division from late July, with spring dates set by year parity, for stage -1. | high | opus |  |
| 0x5538d0 | 99 | `DenPrm::create_table` | thiscall(DenPrm* this) ret 0, returns 1 on success and 0 on failure | Allocates the 12-row table, fills it with the Danish Premier Division clubs, sets the prize fund and pays each club 100000. | high | opus |  |
| 0x553a00 | 40 | `DenPrm::set_up_rules` | thiscall(DenPrm* this) ret 0, returns 1 | Sets the Danish Premier Division rule bytes, with no upper league and the First Division below, and builds the schedule for stage -1. | high | opus |  |
| 0x553aa0 | 163 | `DenPrm::start_new_season` | thiscall(DenPrm* this) ret 0 | Runs Danish promotion and relegation, refreshes the Second Division from the lower division, rebuilds the table and fixtures and restarts the lower leagues. | high | opus |  |
| 0x553cb0 | 159 | `DenPrm::refresh_second_division_clubs` | thiscall(DenPrm* this) ret 0 | Promotes four shuffled Danish lower division clubs into the Second Division and moves relegated Second Division clubs down to the lower division. | high | sonnet |  |
