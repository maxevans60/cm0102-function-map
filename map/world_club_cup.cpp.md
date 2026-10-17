# world_club_cup.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x92b4b0 | 133 (+2 unwind) | `WorldClubCup::WorldClubCup` | thiscall(WorldClubCup* this, short year, ClubComp* record) ret 8, returns this | Constructs the World Club Cup on the Cup base, picks its two qualifiers, builds the round table and fixture tree and Comp_Stats. | high | opus | club-world.md |
| 0x92b680 | 11 | `WorldClubCup::`scalar deleting destructor'` | thiscall(WorldClubCup* this, unsigned flags) ret 4, returns this | Runs the destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x92b6a0 | 62 (+1 unwind) | `WorldClubCup::~WorldClubCup` | thiscall(WorldClubCup* this) ret 0 | Destroys the cup: frees the qualifier record, round table, fixture lists and Comp_Stats object, then runs the Cup destructor. | high | opus |  |
| 0x92b770 | 98 | `WorldClubCup::create_round_table` | thiscall(WorldClubCup* this, char stage, short* round_count, short* extra, int* out) ret 0x10, returns round table | Builds the single-round table of the one-match final with its draw and match dates for the whole-cup stage. | high | opus | 2026-10-16-sweep-europe.md |
| 0x92b8b0 | 368 | `WorldClubCup::pick_qualifiers` | thiscall(WorldClubCup* this) ret 0, returns 1, 0 on error, -1 on allocation failure | Picks the European and South American representatives, taking the continental winner or a random club above reputation 5000 of each continent. | high | opus | 2026-10-16-sweep-europe.md |
| 0x92bda0 | 132 | `WorldClubCup::start_new_season` | thiscall(WorldClubCup* this) ret 0 | Starts the new season: frees the round data, archives Comp_Stats, moves the year on by one and picks qualifiers and rounds again. | high | opus |  |
