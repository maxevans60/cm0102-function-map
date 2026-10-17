# mini_league.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x766500 | 203 (+3 unwind) | `MiniLeague::MiniLeague` | thiscall(MiniLeague* this, short team_count, League* source, int id, Date start_date, char p6, char p7, char* flags_a[4], char* flags_b[4], short p10, char p11, short p12) ret 0x2c, returns this | Constructs a friendly mini league on the League base, builds its schedule, table, fixtures and statistics block, and reports an error on failure. | high | opus |  |
| 0x7667e0 | 11 | `MiniLeague::`scalar deleting destructor'` | thiscall(MiniLeague* this, unsigned flags) ret 4, returns this | Runs the mini league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x766800 | 55 (+2 unwind) | `MiniLeague::MiniLeague` | thiscall(MiniLeague* this, int id) ret 4, returns this | Constructs a four team mini league for a loaded game and reads its state from the competition temp file, reporting an error on failure. | high | opus |  |
| 0x7668f0 | 37 (+2 unwind) | `MiniLeague::~MiniLeague` | thiscall(MiniLeague* this) ret 0 | Destroys a mini league by freeing its table, its schedule buffer and statistics block, then running the League destructor. | high | opus |  |
| 0x766970 | 198 (+1 unwind) | `MiniLeague::create_schedule` | thiscall(MiniLeague* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds a three round schedule on consecutive days from the start date for the whole mini league stage, or returns null for other stages. | high | opus |  |
| 0x766bf0 | 76 | `MiniLeague::alloc_table` | thiscall(MiniLeague* this, Club** clubs) ret 4, returns 1 or 0 | Allocates the league table of 59 byte rows for the team count and places each given club in a row, reporting an error on failure. | high | opus |  |
| 0x766cf0 | 42 | `MiniLeague::load_extra_data` | thiscall(MiniLeague* this, FILE* stream) ret 4, returns 1 or 0 | Reads the eight byte start date of the mini league from a saved game stream and reports an error on a short read. | high | opus |  |
| 0x766d90 | 9 | `MiniLeague::save_extra_data` | thiscall(MiniLeague* this, FILE* stream) ret 4 | Writes the eight byte start date of the mini league to a saved game stream. | high | opus |  |
| 0x766db0 | 25 | `MiniLeague::set_up_rules` | thiscall(MiniLeague* this) ret 0, returns 1 | Resets the mini league rule fields and points values, then rebuilds its schedule through create_schedule. | high | opus |  |
