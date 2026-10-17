# por_second_b.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7d1920 | 168 (+2 unwind) | `PorSecondB::PorSecondB` | thiscall(PorSecondB* this, short year, void* comp_record) ret 8, returns this | Constructs the Portuguese Segunda B league, loads it or sets rules, fills the main table, builds fixtures and creates the two extra zone stages. | high | opus |  |
| 0x7d1b60 | 11 | `PorSecondB::`scalar deleting destructor'` | thiscall(PorSecondB* this, unsigned flags) ret 4, returns this | Runs the PorSecondB destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x7d1b80 | 60 (+1 unwind) | `PorSecondB::~PorSecondB` | thiscall(PorSecondB* this) ret 0 | Destroys the Segunda B league, freeing its table, schedule, zone stages and Comp_Stats, then runs the League destructor. | high | opus |  |
| 0x7d1c40 | 824 | `PorSecondB::create_schedule` | thiscall(PorSecondB* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the 38-round schedule template for the main league and the zone stages, with dates by season year. | high | opus |  |
| 0x7d2400 | 165 | `PorSecondB::create_table` | thiscall(PorSecondB* this) ret 0, returns 1 when 20 rows are filled | Moves zone clubs into this division in 2001, then allocates the 20-row table and fills it with the clubs of the first zone. | high | sonnet |  |
| 0x7d2610 | 39 | `PorSecondB::set_up_rules` | thiscall(PorSecondB* this) ret 0, returns 1 | Sets the points, tiebreak and promotion rules of the Segunda B league and builds its schedule. | high | opus |  |
| 0x7d26b0 | 147 | `PorSecondB::start_new_season` | thiscall(PorSecondB* this) ret 0 | Clears last season's table and zone stages, increments the year, rebuilds rules, table, fixtures and zone stages, then renews officials. | high | opus |  |
| 0x7d2870 | 230 (+1 unwind) | `PorSecondB::create_zone_stage` | thiscall(PorSecondB* this, char zone) ret 4 | Collects the 20 clubs of one of the two extra zones and creates a League_Stage for them in the stage array. | high | sonnet |  |
| 0x7d2b80 | 95 | `PorSecondB::get_club_array` | thiscall(PorSecondB* this, Club*** out_clubs, short* out_count) ret 8 | Returns an array of all 60 clubs of the main table and the two zone stages with its count. | high | opus |  |
| 0x7d2cd0 | 123 | `PorSecondB::set_predicted_positions` | thiscall(PorSecondB* this) ret 0 | Sorts the clubs of the main table and each zone stage by strength and stores interleaved predicted positions. | high | opus |  |
