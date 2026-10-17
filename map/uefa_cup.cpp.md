# uefa_cup.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x9022e0 | 139 (+2 unwind) | `UefaCup::UefaCup` | thiscall(UefaCup* this, short year, ClubComp* record), returns this, ret 8 | Builds the UEFA Cup on the Cup base, refreshes the seeding, lists the entrants and builds the round table. | high | opus |  |
| 0x9024d0 | 11 | `UefaCup::`scalar deleting destructor'` | thiscall(UefaCup* this, unsigned flags), returns this, ret 4 | Runs the UEFA Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x9024f0 | 62 (+1 unwind) | `UefaCup::~UefaCup` | thiscall(UefaCup* this), ret 0 | Restores the vtable, frees the entrant, round and tie tables and the Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x9025c0 | 465 | `UefaCup::create_round_table` | thiscall(UefaCup* this, char stage, short* round_count, short* extra, int* is_league), returns round table, ret 0x10 | Allocates the UEFA Cup round table and sets the draw and match dates of each round, with a qualifying round when +0xb2 is positive. | high | opus | 2026-10-16-sweep-europe.md |
| 0x902b90 | 251 | `UefaCup::build_entrants` | thiscall(UefaCup* this), returns 1, 0 or -1, ret 0 | Lists the clubs with a UEFA Cup place, adds spare clubs up to 118, sorts the list and reserves 27 slots for later entrants. | high | opus | 2026-10-16-sweep-europe.md |
| 0x902ee0 | 144 | `UefaCup::start_new_season` | thiscall(UefaCup* this), ret 0 | Starts a new UEFA Cup season: frees the tables, archives the stats, adds one to the year and rebuilds the entrants and rounds. | high | opus |  |
| 0x9030b0 | 16 | `UefaCup::set_up_rounds` | thiscall(UefaCup* this), returns 1, ret 0 | Sets the UEFA Cup prize fund to 3,000,000 and builds its round table. | high | opus |  |
| 0x9030e0 | 23 | `UefaCup::update_staff_records_for_status` | thiscall(UefaCup* this, Club* club, char outcome, int arg3, int arg4, Fixture* fixture, int arg6), ret 0x18 | Clears the club's European competition field when the outcome is 1, 2 or -1, then runs the Cup base staff record update. | high | opus |  |
| 0x903120 | 145 | `UefaCup::collect_club_list` | thiscall(UefaCup* this, Club*** out_clubs, char kind), returns club count, ret 8 | Allocates an array of the UEFA Cup clubs, either all entrants or the clubs of one round picked by kind 1, 2 or 3. | high | opus |  |
| 0x903300 | 19 | `UefaCup::load_extra_data` | thiscall(UefaCup* this, FILE* file), returns 1, ret 4 | Reads the qualifying-round byte at +0xb2 from the save file when the save version is above 0x3e003, else sets it to zero. | high | opus |  |
| 0x903340 | 9 | `UefaCup::save_extra_data` | thiscall(UefaCup* this, FILE* file), ret 4 | Writes the qualifying-round byte at +0xb2 to the save file. | high | opus |  |
