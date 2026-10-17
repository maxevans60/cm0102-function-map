# eng_conf.cpp: 7 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x56db60 | 158 (+2 unwind) | `EngConf::EngConf` | thiscall(EngConf* this, short comp_id, Nation* owner) ret 8, returns this | Constructs the Football Conference league, loads its saved state or sets its rules, builds the table and fixtures and sorts the table. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x56dd80 | 11 | `EngConf::`scalar deleting destructor'` | thiscall(EngConf* this, unsigned flags) ret 4, returns this | Destroys the Conference league and frees its memory when bit 0 of the flags is set. | high | opus |  |
| 0x56dda0 | 60 (+1 unwind) | `EngConf::~EngConf` | thiscall(EngConf* this) ret 0 | Restores the Conference vtable, frees the table, schedule and stage objects and the Comp_Stats object, then runs the League destructor. | high | opus |  |
| 0x56de60 | 1555 | `EngConf::create_schedule` | thiscall(EngConf* this, char stage, short* round_count, short* out2, int* out_flag) ret 0x10, returns schedule pointer | Builds the Conference league round dates for stage -1, and a three-round play-off schedule for stage 0. | high | opus |  |
| 0x56ecb0 | 99 | `EngConf::create_table` | thiscall(EngConf* this) ret 0, returns 1 on success and 0 on failure | Builds the 22-row Conference table from the clubs in its division, then sets the prize fund and pays the clubs. | high | opus |  |
| 0x56ede0 | 39 | `EngConf::set_up_rules` | thiscall(EngConf* this) ret 0, returns 1 | Sets the Conference league rules for points, tiebreaks and promotion places, then builds its schedule through the create schedule virtual. | high | opus |  |
| 0x56ee80 | 143 | `EngConf::start_new_season` | thiscall(EngConf* this) ret 0 | Frees last season's Conference data, archives the stats, moves the year on and rebuilds the rules, table and fixtures. | high | opus |  |
