# ire_leinster_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6364a0 | 132 (+2 unwind) | `IreLeinsterCup::IreLeinsterCup` | thiscall(IreLeinsterCup* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Leinster Senior Cup on Cup, then loads saved data or picks its clubs, builds rounds and fixture tree and Comp_Stats. | high | opus |  |
| 0x636670 | 11 | `IreLeinsterCup::`scalar deleting destructor'` | thiscall(IreLeinsterCup* this, unsigned flags), returns this, ret 4 | Runs the IreLeinsterCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x636690 | 62 (+1 unwind) | `IreLeinsterCup::~IreLeinsterCup` | thiscall(IreLeinsterCup* this), ret 0 | Destroys the Leinster cup, freeing its club list, round table, per-round arrays and Comp_Stats before the Cup destructor runs. | high | opus |  |
| 0x636760 | 213 | `IreLeinsterCup::create_round_table` | thiscall(IreLeinsterCup* this, char stage, short* round_count, short* out2, int* out_flag), returns round table or null, ret 0x10 | Builds the four knockout rounds of the 16-club Leinster cup, from August to a March final, for stage -1. | high | opus |  |
| 0x636a80 | 123 | `IreLeinsterCup::select_clubs` | thiscall(IreLeinsterCup* this), returns 1 or -1 on allocation failure, ret 0 | Fills the 16-club entry list with four Leinster Senior League clubs and the Leinster clubs of the Irish Premier and First Divisions. | high | opus |  |
| 0x636c20 | 132 | `IreLeinsterCup::start_new_season` | thiscall(IreLeinsterCup* this), ret 0 | Frees last season's club list and rounds, archives the statistics, advances the year and selects clubs and rounds again. | high | opus |  |
| 0x636d20 | 29 | `IreLeinsterCup::start_new_season_fragment_636d20` | none, false entry inside 0x636c20, ret 0 | Marks a false function start inside IreLeinsterCup::start_new_season, on the failure path of the set_up_rounds call. | high | opus |  |
