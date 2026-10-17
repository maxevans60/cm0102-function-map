# mini_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x765bf0 | 152 (+3 unwind) | `MiniCup::MiniCup` | thiscall(MiniCup* this, Club** clubs, int comp_id, Date start_date, short year, char p6, short p7) ret 0x18, returns this | Constructs a four-club mini cup, stores its entrants and dates, builds the round table and maps the fixture tree. | high | opus |  |
| 0x765e10 | 11 | `MiniCup::`scalar deleting destructor'` | thiscall(MiniCup* this, unsigned flags) ret 4, returns this | Runs the mini cup destructor and frees the object when the low flag bit is set. | high | opus |  |
| 0x765e30 | 26 (+2 unwind) | `MiniCup::MiniCup` | thiscall(MiniCup* this, int comp_id) ret 4, returns this | Constructs a mini cup from saved data by building the base cup and loading its state from the temporary file. | high | opus |  |
| 0x765ea0 | 62 (+2 unwind) | `MiniCup::~MiniCup` | thiscall(MiniCup* this) ret 0 | Destroys a mini cup by freeing its entrant table, round table, tie arrays and stats object, then running the Cup destructor. | high | opus |  |
| 0x765f70 | 196 (+1 unwind) | `MiniCup::create_round_table` | thiscall(MiniCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table or 0 | Builds the three-round table of a mini cup from its start date when called for the whole cup. | high | opus |  |
| 0x766290 | 69 | `MiniCup::set_up_clubs` | thiscall(MiniCup* this, Club** clubs) ret 4, returns 1 or 0 | Sets the cup's club count to four and copies the four given clubs into a new six-byte entrant table. | medium | opus |  |
| 0x766380 | 86 | `MiniCup::load_extra_data` | thiscall(MiniCup* this, FILE* file) ret 4, returns 1 | Reads the mini cup start date and its extra word from the temporary file, ending the game on a short read. | high | opus |  |
| 0x7664c0 | 20 | `MiniCup::save_extra_data` | thiscall(MiniCup* this, FILE* file) ret 4 | Writes the mini cup start date and its extra word to the temporary file. | high | opus |  |
