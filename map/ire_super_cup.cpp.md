# ire_super_cup.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x63acd0 | 109 (+2 unwind) | `IreSuperCup::IreSuperCup` | thiscall(IreSuperCup* this, short year, CompRecord* comp), returns this, ret 8 | Constructs the Irish Super Cup on League, then loads saved data or sets its rules, schedule and Comp_Stats with the table left empty. | high | opus |  |
| 0x63ae80 | 11 | `IreSuperCup::`scalar deleting destructor'` | thiscall(IreSuperCup* this, unsigned flags), returns this, ret 4 | Runs the IreSuperCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x63aea0 | 60 (+1 unwind) | `IreSuperCup::~IreSuperCup` | thiscall(IreSuperCup* this), ret 0 | Destroys the Irish Super Cup, freeing its table, schedule, stage objects and Comp_Stats before the League destructor runs. | high | opus |  |
| 0x63af60 | 116 | `IreSuperCup::create_schedule` | thiscall(IreSuperCup* this, char stage, short* round_count, short* out2, int* out_flag), returns schedule pointer, ret 0x10 | Builds the three-round Super Cup template for stage -1, with rounds on 27 June, 29 June and 1 July. | high | opus |  |
| 0x63b0c0 | 194 | `IreSuperCup::create_table` | thiscall(IreSuperCup* this), returns 1 when four clubs are found, ret 0 | Fills the four-club table with Irish clubs entered in the Champions League, UEFA Cup and Intertoto Cup, then Premier Division clubs. | high | opus |  |
| 0x63b300 | 117 | `IreSuperCup::update_for_date` | thiscall(IreSuperCup* this, Date* today, int full_update) ret 8 | Builds the table, fixtures and predicted positions once in the season year, then runs the base League daily update. | high | opus |  |
| 0x63b4c0 | 37 | `IreSuperCup::set_up_rules` | thiscall(IreSuperCup* this), returns 1, ret 0 | Sets the Super Cup rule bytes, with no league above or below and one meeting, and builds the schedule for stage -1. | high | opus |  |
| 0x63b550 | 78 | `IreSuperCup::start_new_season` | thiscall(IreSuperCup* this), ret 0 | Frees the table and schedule, archives the stats, deletes the stage objects, moves to the next year and sets up the rules again. | high | opus |  |
