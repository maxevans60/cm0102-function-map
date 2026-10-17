# sub_league.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x88c6d0 | 186 (+1 unwind) | `SubLeague::SubLeague` | thiscall(SubLeague* this, short team_count, int* club_ids, int club_filter, int filter_arg, Date* from, Date* to, int comp_index, byte flag_c2, byte flag_c3, byte* rule_bytes, int scan_arg, LLIST* fixtures_or_null) ret 0x30 | Constructs a mini league table for a given set of clubs, fills it from the fixtures they played against each other and sorts it. | high | opus |  |
| 0x88c970 | 11 | `SubLeague::`scalar deleting destructor'` | thiscall(SubLeague* this, unsigned flags), returns this, ret 4 | Destroys the sub league and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x88c990 | 21 (+1 unwind) | `SubLeague::~SubLeague` | thiscall(SubLeague* this), ret 0 | Destroys the sub league by restoring its vtable, freeing its table rows and running the League base destructor. | high | opus |  |
| 0x88c9f0 | 152 (+1 unwind) | `SubLeague::add_results_between_members` | thiscall(SubLeague* this, int club_filter, int filter_arg, Date* from, Date* to, int comp_index, int scan_arg, LLIST* fixtures_or_null) returns 1, ret 0x1c | Scans played fixtures in a date window and adds each match whose home and away clubs are both in the sub league table. | high | opus |  |
