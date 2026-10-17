# world_cup_awards.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x92fc10 | 35 (+1 unwind) | `WorldCupAwards::WorldCupAwards` | thiscall(WorldCupAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the World Cup awards object on the NationAwards base, sets its vtable and fields, then loads saved data or creates fresh award objects. | high | opus |  |
| 0x92fc80 | 108 (+2 unwind) | `WorldCupAwards::init_awards` | thiscall(WorldCupAwards* this, FILE* load_source or 0) ret 4 | Allocates the two-entry award table and constructs one yearly player award and one team award, reporting an assert error if the table allocation fails. | high | opus |  |
| 0x92fdf0 | 52 | `WorldCupAwards::daily_update` | thiscall(WorldCupAwards* this, Date* date) ret 4 | In a World Cup year, on the date built as day 13 of month index 6, picks the top three players and the team award winners. | high | opus |  |
