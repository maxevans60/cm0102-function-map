# league_stage.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x68b100 | 254 (+1 unwind) | `League_Stage::League_Stage` | thiscall(League_Stage* this, Comp* parent, short teams, Club** team_list, short p5, int p6, void* fixture_dates, short date_count, ...) ret 0x58 | Builds a league stage of a cup, sets up its table rows and fixtures, and sorts the table. | high | opus | 2026-10-16-sweep-europe.md |
| 0x68b4d0 | 11 | `League_Stage::`scalar deleting destructor'` | thiscall(League_Stage* this, unsigned flags) ret 4, returns this | Runs the league stage destructor and frees the object when the low flag bit is set. | high | opus |  |
| 0x68b4f0 | 114 (+1 unwind) | `League_Stage::League_Stage` | thiscall(League_Stage* this, short team_count, short entry_count) ret 8, returns this | Constructs an empty league stage for loading, allocating its 0x3b-byte team rows and 0x41-byte entries before the saved data is read. | high | opus |  |
| 0x68b6a0 | 34 (+1 unwind) | `League_Stage::~League_Stage` | thiscall(League_Stage* this) ret 0 | Destroys a league stage by freeing its table, entry buffer and fixture buffer, then running the League destructor. | high | opus |  |
| 0x68b720 | 1399 | `League_Stage::load_from_file` | thiscall(League_Stage* this, FILE* file) ret 4 | Reads a league stage field by field from the open temporary file and turns the stored club indices back into club pointers. | high | opus |  |
| 0x68ca40 | 479 | `League_Stage::save_to_file` | thiscall(League_Stage* this, FILE* file) ret 4 | Writes a league stage and its team rows to the open temporary file, storing club pointers as indices and restoring them after. | high | opus |  |
