# eng_fa_cup.cpp: 12 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x56f040 | 135 (+2 unwind) | `EngFaCup::EngFaCup` | thiscall(EngFaCup* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the FA Cup, loads its saved state or allocates its 152-team table, builds the round table and the fixture tree. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x56f230 | 11 | `EngFaCup::`scalar deleting destructor'` | thiscall(EngFaCup* this, unsigned flags) ret 4, returns this | Destroys the FA Cup and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x56f250 | 62 (+1 unwind) | `EngFaCup::~EngFaCup` | thiscall(EngFaCup* this) ret 0 | Restores the FA Cup vtable, frees the team, round and tie arrays and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x56f320 | 456 | `EngFaCup::create_round_table` | thiscall(EngFaCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table pointer | Builds the nine FA Cup rounds from September to May, and moves round entry counts for exempt clubs that skip early rounds. | high | opus |  |
| 0x56fab0 | 668 | `EngFaCup::collect_entrants` | thiscall(EngFaCup* this) ret 0, returns 1 when the 152 entries fill, 0 when short, -1 on allocation failure | Collects the 152 FA Cup entrants from the league divisions, the Conference and non-league clubs, and handles English clubs in the Club World Championship. | medium | opus | 2026-10-16-season-change-points.md |
| 0x570390 | 133 | `EngFaCup::start_new_season` | thiscall(EngFaCup* this) ret 0 | Frees last season's FA Cup data, archives the stats, moves the year on and reallocates the team table and rounds. | high | opus |  |
| 0x570550 | 213 (+1 unwind) | `EngFaCup::update_for_date` | thiscall(EngFaCup* this, Date* today, int phase) ret 8 | Asks the human manager on 1 September 1999 about the fifth-round entry, collects the entrants each 3 September, then runs the base cup update. | high | opus |  |
| 0x570830 | 39 | `EngFaCup::load_extra_data` | thiscall(EngFaCup* this, FILE* file) ret 4, returns 1 | Reads the FA Cup exemption flags from a save file, and sets the fifth-round choice to 3 for older save versions. | high | opus |  |
| 0x5708a0 | 26 | `EngFaCup::save_extra_data` | thiscall(EngFaCup* this, FILE* file) ret 4 | Writes the three FA Cup exemption and fifth-round choice flags to a save file. | high | opus |  |
| 0x5708f0 | 22 | `fa_cup_open_fifth_round_entry_screen` | cdecl(int news_item, int news_slot) ret 0 | Opens the screen that asks whether to enter the FA Cup at the fifth round, and stores the two news arguments as screen parameters. | medium | opus |  |
| 0x570940 | 127 | `fa_cup_draw_fifth_round_entry_screen` | cdecl(void) ret 0 | Draws the Please Confirm screen that asks whether to enter the FA Cup at the fifth round, with Yes and No buttons. | high | opus |  |
| 0x570ae0 | 95 | `fa_cup_handle_fifth_round_entry_screen` | cdecl(short button) ret 0, returns -9 to close the screen or the menu bar result | Handles the fifth-round entry screen, sets the FA Cup choice flag on Yes, updates the news item and passes other input to the menu bar. | medium | opus |  |
