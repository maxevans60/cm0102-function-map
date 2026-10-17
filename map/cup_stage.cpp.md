# cup_stage.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x522e00 | 196 (+1 unwind) | `Cup_Stage::Cup_Stage` | thiscall(Cup_Stage *this, Comp *parent, short team_count, int *teams, short fixture_count, int arg, void *fixture_template, short s, char b1, char b2, short s2, char b3, int link_mode, int seed_by_order, int arg15, char *seeds) ret 0x3c | Constructs a cup stage, copies the fixture templates and team list with seeds, then links the fixture tree. | high | opus | 2026-10-16-sweep-europe.md, int-world.md |
| 0x5230c0 | 11 | `Cup_Stage::`scalar deleting destructor'` | thiscall(Cup_Stage *this, unsigned flags) ret 4 | Runs the cup stage destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5230e0 | 153 (+1 unwind) | `Cup_Stage::Cup_Stage` | thiscall(Cup_Stage *this, short team_count, short round_count, short *ties_per_round) ret 0xc | Constructs an empty cup stage for loading, allocating the team table, the round table and one tie array per round. | high | opus |  |
| 0x523300 | 42 | `Cup_Stage::~Cup_Stage` | thiscall(Cup_Stage *this) ret 0 | Restores the cup stage vtable, frees the team table, round table and per-round tie arrays, then runs the Cup destructor. | high | opus |  |
| 0x523380 | 794 | `Cup_Stage::load_from_file` | thiscall(Cup_Stage *this, FILE *file) ret 4 | Reads the cup stage fields, round table, team table and tie arrays from the temporary file and turns stored indices back into pointers. | high | opus |  |
| 0x523eb0 | 274 | `Cup_Stage::save_to_file` | thiscall(Cup_Stage *this, FILE *file) ret 4 | Writes the cup stage fields, round table, team table and tie arrays to the temporary file, storing team pointers as indices. | high | opus |  |
| 0x5241e0 | 730 | `Cup_Stage::map_fixture_tree` | thiscall(Cup_Stage *this) ret 0, returns 1 on success, -1 on failure | Allocates and resets the per-round tie arrays, links each tie winner to a slot in the next round and seeds the first-round ties. | high | opus |  |
| 0x524550 | 626 | `Cup_Stage::map_fixture_tree_fragment_524550` | fragment of Cup_Stage::map_fixture_tree, ESI = this, register state of the parent, no own prologue | Holds the loop test and later code of Cup_Stage::map_fixture_tree, which the decompiler split off as a separate function. | medium | opus |  |
