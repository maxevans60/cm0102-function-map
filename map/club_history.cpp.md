# club_history.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x442ab0 | 253 (+2 unwind) | `Club_History::Club_History` | thiscall(Club_History* this, void* archive_or_null) ret 4, returns this | Constructs the club history store: checks for the game CD, opens the league and cup history lists, then loads or allocates club records. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x442e20 | 32 | `Club_History::~Club_History` | thiscall(Club_History* this) ret 0 | Destroys the club history store: deletes both history lists and frees the per-club record array. | high | opus |  |
| 0x442e80 | 377 | `Club_History::record_comp_season` | thiscall(Club_History* this, Comp* comp) ret 4, returns 1 or 0 | Adds the finished season of a competition to each club's history: league position and table record for divisions, furthest round for cups. | high | opus | 2026-10-16-research-name-check.md, 2026-10-16-sweep-season-end.md |
| 0x443380 | 130 (+2 unwind) | `Club_History::get_league_history` | thiscall(Club_History* this, Club* club) ret 4, returns LLIST* or null | Builds a list of a club's league seasons, newest first, with the current season added when it is not complete. | high | opus |  |
| 0x443520 | 174 (+2 unwind) | `Club_History::get_cup_history` | thiscall(Club_History* this, Club* club) ret 4, returns LLIST* or null | Builds a list of a club's cup runs, with the current progress in each running cup first and the stored seasons after. | high | opus |  |
| 0x443770 | 199 (+1 unwind) | `Club_History::get_league_comp_ids` | thiscall(Club_History* this, LLIST* league_history) ret 4, returns LLIST* or null | Collects the distinct competition ids from a club's league history list, sorts them and returns them as a new list. | high | opus |  |
| 0x443a20 | 199 (+1 unwind) | `Club_History::get_cup_comp_ids` | thiscall(Club_History* this, LLIST* cup_history) ret 4, returns LLIST* or null | Collects the distinct competition ids from a club's cup history list, sorts them and returns them as a new list. | high | opus |  |
| 0x443cd0 | 190 | `Club_History::load` | thiscall(Club_History* this, void* archive) ret 4, returns 1 or 0 | Reads the club count and the per-club history records from the club history.dat entry of a saved game archive. | high | opus |  |
| 0x443f50 | 168 | `Club_History::save` | thiscall(Club_History* this, void* archive) ret 4, returns 1 or 0 | Writes the club count and the per-club history records to the club history.dat entry of a saved game archive. | high | opus |  |
| 0x444190 | 248 (+1 unwind) | `club_history_get_current_league_record` | cdecl(Club* club, LeagueHistoryRecord* out, int* out_complete, Stage** out_stage, int use_date_rule) ret 0, returns 1 or 0 | Finds a club in the current table of its division and fills a league history record with position and table figures. | high | opus | 2026-10-15-team-views-frame-inventory.md |
| 0x444500 | 13 | `compare_int_ids` | cdecl(const int* a, const int* b) ret 0, returns int | Compares two ints for qsort but returns 1 whenever they differ and 0 when equal, so it never orders them. | medium | opus |  |
