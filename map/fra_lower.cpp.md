# fra_lower.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5bd600 | 178 (+1 unwind) | `FraLower::FraLower` | thiscall(FraLower* this, short year), ret 4 | Constructs the French lower league on League, picks 40 clubs from the third division and one lower division, then builds fixtures in two halves. | medium | opus | fra.md |
| 0x5bd850 | 11 | `FraLower::`scalar deleting destructor'` | thiscall(FraLower* this, unsigned flags), ret 4, returns this | Runs the French lower league destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5bd870 | 52 (+1 unwind) | `FraLower::~FraLower` | thiscall(FraLower* this), ret 0 | Destroys the French lower league by freeing its table, schedule and stage objects, then runs the League destructor. | high | opus |  |
| 0x5bd920 | 977 | `FraLower::create_schedule` | thiscall(FraLower* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the 38-round schedule template of the French lower league from late July to late May for stage -1 and returns null otherwise. | high | opus |  |
| 0x5be230 | 81 | `FraLower::create_table` | thiscall(FraLower* this, Club** clubs), ret 4, returns bool | Allocates the 20-row table and fills it from a list of 20 clubs, with a flag on each club of the third division. | high | opus |  |
