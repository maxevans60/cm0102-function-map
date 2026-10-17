# ita_c1_super.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63c5e0 | 128 (+2 unwind) | `ItaC1Super::ItaC1Super` | thiscall(ItaC1Super* this, short year, void* comp_record) ret 8 | Constructs the Serie C1 Super Cup on Cup and, when no saved data loads, sets up its empty two-club list, rounds, tie tree and stats. | high | opus |  |
| 0x63c7a0 | 11 | `ItaC1Super::`scalar deleting destructor'` | thiscall(ItaC1Super* this, unsigned flags) ret 4, returns this | Runs the Serie C1 Super Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x63c7c0 | 62 (+1 unwind) | `ItaC1Super::~ItaC1Super` | thiscall(ItaC1Super* this) ret 0 | Destroys the Serie C1 Super Cup by freeing its team list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x63c890 | 98 | `ItaC1Super::create_round_table` | thiscall(ItaC1Super* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* or null | Builds the one-round table of the Serie C1 Super Cup with its draw and match dates for two teams over two legs. | high | opus |  |
| 0x63c9d0 | 58 | `ItaC1Super::init_team_list` | thiscall(ItaC1Super* this) ret 0, returns 1 or -1 | Sets the team count to two and allocates the 12-byte team list at +0xa7 with both club slots cleared, reporting an error on allocation failure. | medium | opus |  |
| 0x63caa0 | 125 | `ItaC1Super::start_new_season` | thiscall(ItaC1Super* this) ret 0 | Clears the finished Serie C1 Super Cup, archives its stats, moves the year on and sets up the team list and rounds again. | high | opus |  |
