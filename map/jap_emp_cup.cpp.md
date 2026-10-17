# jap_emp_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x661d30 | 132 (+2 unwind) | `JapEmpCup::JapEmpCup` | thiscall(JapEmpCup* this, short id, int parent) ret 8, returns this | Constructs the Emperor's Cup on Cup, then loads its saved state or collects the entrants, builds the round table, fixture tree and statistics. | high | opus |  |
| 0x661f00 | 11 | `JapEmpCup::`scalar deleting destructor'` | thiscall(JapEmpCup* this, unsigned flags) ret 4, returns this | Runs the Emperor's Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x661f20 | 62 (+1 unwind) | `JapEmpCup::~JapEmpCup` | thiscall(JapEmpCup* this) ret 0 | Destroys the Emperor's Cup by freeing its entrant list, round table, tie arrays and statistics, then runs the Cup destructor. | high | opus |  |
| 0x661ff0 | 325 | `JapEmpCup::create_round_table` | thiscall(JapEmpCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table | Builds the seven-round table of the Emperor's Cup with draw dates, match dates and round rules for stage -1. | high | opus |  |
| 0x6624f0 | 313 | `JapEmpCup::collect_entrants` | thiscall(JapEmpCup* this) ret 0, returns 1 when full, 0 or -1 on failure | Fills the 80-entry six-byte entrant list with shuffled Japanese lower clubs, then J2 and J1 clubs, and sorts the seeded part. | medium | opus |  |
| 0x662950 | 132 | `JapEmpCup::start_new_season` | thiscall(JapEmpCup* this) ret 0 | Frees last season's cup data, archives the statistics, advances the year and rebuilds the entrants and rounds. | high | opus |  |
| 0x662b00 | 16 | `JapEmpCup::set_up_rounds` | thiscall(JapEmpCup* this) ret 0, returns 1 | Sets a prize fund of 7000000 and builds the round table of the Emperor's Cup. | high | opus |  |
