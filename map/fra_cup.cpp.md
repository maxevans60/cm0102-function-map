# fra_cup.cpp: 9 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5ba130 | 133 (+2 unwind) | `FraCup::FraCup` | thiscall(FraCup* this, short season_year, int comp_record) ret 8, returns this | Constructs the Coupe de France, loads it from disk or collects 222 entrants, sets a 1000000 prize fund and builds rounds, fixture tree and stats. | high | opus |  |
| 0x5ba300 | 11 | `FraCup::`scalar deleting destructor'` | thiscall(FraCup* this, unsigned flags) ret 4, returns this | Runs the FraCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x5ba320 | 62 (+1 unwind) | `FraCup::~FraCup` | thiscall(FraCup* this) ret 0 | Destroys the Coupe de France by freeing its entrant list, round table, tie arrays and stats, then runs the Cup destructor. | high | opus |  |
| 0x5ba3f0 | 398 | `FraCup::create_round_table` | thiscall(FraCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns Round* | Builds the nine-round Coupe de France table with draw dates, match dates, round codes 60 to 150 and entry counts for stage -1. | high | opus |  |
| 0x5baa50 | 300 | `FraCup::collect_entrants` | thiscall(FraCup* this) ret 0, returns 1 when 222 entries fill, 0 when short, -1 on allocation failure | Fills the 222-entry Coupe de France entrant list with National, CFA and lower French clubs first, then Second and First Division clubs. | high | opus |  |
| 0x5bae50 | 132 | `FraCup::start_new_season` | thiscall(FraCup* this) ret 0 | Frees last season's cup data, archives the stats, advances the year and rebuilds entrants, rules, rounds and rankings. | high | opus |  |
| 0x5bb000 | 16 | `FraCup::set_up_rounds` | thiscall(FraCup* this) ret 0, returns 1 | Sets a prize fund of 1000000 and builds the round table of the cup through slot 15. | high | opus |  |
| 0x5bb030 | 63 | `FraCup::club_in_higher_division` | thiscall(FraCup* this unused, Club* a, Club* b) ret 8, returns b or 0 | Returns the second club when the first plays in the top three French divisions and the second sits at least two levels lower, else zero. | high | opus |  |
| 0x5bb100 | 26 | `FraCup::set_fixture_substitutes` | thiscall(FraCup* this, Fixture* fixture) ret 4 | Packs the cup's named and used substitute counts into the fixture substitutes word, with five named substitutes for the final. | high | opus |  |
