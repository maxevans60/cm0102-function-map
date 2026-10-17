# ire_chal_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6340a0 | 132 (+2 unwind) | `IreChalCup::IreChalCup` | thiscall(IreChalCup* this, short year, void* comp_record), ret 8, returns this | Constructs the Irish Challenge Cup on Cup and, when no saved data loads, collects its entrants and builds its rounds, tie tree, stats and ranking. | high | opus |  |
| 0x634220 | 63 | `IreChalCup::IreChalCup_fragment_634220` | false entry inside IreChalCup::IreChalCup, ret 8 | Misread entry point inside the constructor's error path that shows the Error message box and then ranks the teams. | high | opus |  |
| 0x634270 | 11 | `IreChalCup::`scalar deleting destructor'` | thiscall(IreChalCup* this, unsigned flags), ret 4, returns this | Runs the Irish Challenge Cup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x634290 | 62 (+1 unwind) | `IreChalCup::~IreChalCup` | thiscall(IreChalCup* this), ret 0 | Destroys the Irish Challenge Cup by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x634360 | 289 | `IreChalCup::create_round_table` | thiscall(IreChalCup* this, char stage, short* round_count, short* extra, int* out), ret 0x10, returns Round* or null | Builds the six-round table of the Irish Challenge Cup with draw dates, match dates and team counts from 20 down to the two-team final. | high | opus |  |
| 0x6347d0 | 191 | `IreChalCup::collect_entrants` | thiscall(IreChalCup* this), ret 0, returns 1 or -1 on allocation failure | Fills the 42-entry entrant list with five random clubs from each of four regional leagues and every club of the two national divisions. | high | opus |  |
| 0x634a60 | 132 | `IreChalCup::start_new_season` | thiscall(IreChalCup* this), ret 0 | Frees last season's cup data, archives the stats, moves the year on and rebuilds the entrants, rounds and fixture tree. | high | opus |  |
| 0x634c10 | 16 | `IreChalCup::set_up_rounds` | thiscall(IreChalCup* this), ret 0, returns 1 | Sets the prize fund to 100000 and builds the round table through the create_round_table virtual. | high | opus |  |
