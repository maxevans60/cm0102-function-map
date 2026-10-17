# ire_pres_cup.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x639280 | 126 (+2 unwind) | `IrePresCup::IrePresCup` | thiscall(IrePresCup* this, short comp_id, int owner) ret 8 | Constructs the Irish President's Cup on the Cup base, picks its two entrants and builds the round schedule, fixture tree and Comp_Stats. | high | opus |  |
| 0x639440 | 11 | `IrePresCup::`scalar deleting destructor'` | thiscall(IrePresCup* this, unsigned flags) ret 4, returns this | Runs the IrePresCup destructor and frees the object when bit 0 of the flags is set. | high | opus |  |
| 0x639460 | 62 (+1 unwind) | `IrePresCup::~IrePresCup` | thiscall(IrePresCup* this) ret 0 | Destroys the President's Cup by freeing its entrant list, schedule, round tie arrays and Comp_Stats, then runs the Cup destructor. | high | opus |  |
| 0x639530 | 98 | `IrePresCup::create_round_table` | thiscall(IrePresCup* this, char stage, short* round_count, short* first_id, int* is_league) ret 0x10, returns round table | Builds the single-round date template of the President's Cup, a one-off final. | high | opus |  |
| 0x639670 | 134 | `IrePresCup::collect_entrants` | thiscall(IrePresCup* this) ret 0, returns 1 or -1 on allocation failure | Picks the two highest-placed clubs of last season's top division that are based in Leinster, falling back to the top two clubs. | high | sonnet |  |
| 0x639820 | 125 | `IrePresCup::start_new_season` | thiscall(IrePresCup* this) ret 0 | Frees last season's data, archives the statistics, picks new entrants and sets up the rounds and fixture tree. | high | opus |  |
| 0x6399c0 | 215 | `ire_club_is_in_leinster` | cdecl(Club* club) ret 0, returns bool | Returns true when the city of a club's stadium is Dublin, Bray, Longford, Dundalk, Drogheda, Athlone or Kilkenny. | high | opus |  |
