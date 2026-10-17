# ire_munster_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6387a0 | 132 (+2 unwind) | `IreMunsterCup::IreMunsterCup` | thiscall(IreMunsterCup* this, short comp_id, int owner) ret 8 | Constructs the Munster Senior Cup on the Cup base, collects its 20 entrants, builds the round schedule, fixture tree and Comp_Stats. | high | opus |  |
| 0x638970 | 11 | `IreMunsterCup::`scalar deleting destructor'` | thiscall(IreMunsterCup* this, unsigned flags) ret 4, returns this | Runs the IreMunsterCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x638990 | 62 (+1 unwind) | `IreMunsterCup::~IreMunsterCup` | thiscall(IreMunsterCup* this) ret 0 | Destroys the Munster cup by freeing its entrant list, schedule, round tie arrays and Comp_Stats, then runs the Cup destructor. | high | opus |  |
| 0x638a60 | 251 | `IreMunsterCup::create_round_table` | thiscall(IreMunsterCup* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns round table | Builds the five-round date and tie template of the Munster cup for 20 entrants, from a preliminary round to the final. | high | opus |  |
| 0x638e30 | 218 | `IreMunsterCup::collect_entrants` | thiscall(IreMunsterCup* this) ret 0, returns 1 or -1 on allocation failure | Builds the 20 entrants from the top 16 clubs of one division and four Munster league clubs found by name. | high | opus |  |
| 0x6390d0 | 132 | `IreMunsterCup::start_new_season` | thiscall(IreMunsterCup* this) ret 0 | Frees last season's data, archives the statistics, collects new entrants and sets up the rounds, fixture tree and team ranking. | high | opus |  |
