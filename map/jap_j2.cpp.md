# jap_j2.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6644c0 | 156 (+2 unwind) | `JapJ2::JapJ2` | thiscall(JapJ2* this, short year, void* comp_record) ret 8, returns this | Constructs the Japanese J2 League on League, loads it from the temp file or sets rules, fills the table, builds fixtures, stats and predictions. | high | opus |  |
| 0x6646d0 | 11 | `JapJ2::`scalar deleting destructor'` | thiscall(JapJ2* this, unsigned flags) ret 4, returns this | Runs the J2 League destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x6646f0 | 38 (+1 unwind) | `JapJ2::~JapJ2` | thiscall(JapJ2* this) ret 0 | Destroys the J2 League by freeing its table, its schedule at +0xba and its stats, then runs the League destructor. | high | opus |  |
| 0x664780 | 936 | `JapJ2::create_schedule` | thiscall(JapJ2* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns schedule pointer | Allocates and fills the 44-round schedule of the J2 League with match dates and slots for the current year. | high | opus |  |
| 0x665030 | 86 | `JapJ2::create_table` | thiscall(JapJ2* this) ret 0, returns 1 when the table fills | Fills the 12-club J2 table with every club whose division is the J2 League, and clears the division of any surplus club. | high | opus |  |
| 0x665140 | 38 | `JapJ2::set_up_rules` | thiscall(JapJ2* this) ret 0, returns 1 | Sets the J2 League rules, points and promotion fields, links the J1 League as the next division and builds the schedule. | high | opus |  |
| 0x6651f0 | 125 | `JapJ2::start_new_season` | thiscall(JapJ2* this) ret 0 | Frees last season's table and schedule, archives the stats, advances the year and rebuilds rules, table, fixtures and predictions. | high | opus |  |
