# training_schedule.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8b5000 | 56 | `TRAINING_SCHEDULE::count_players` | thiscall(TRAINING_SCHEDULE *this, LLIST *out or 0, squad entries[50] of 5 bytes, compare function or 0) returns char, ret 0xc | Sorts a squad list if asked, then counts and optionally lists the players on this schedule, all players for Overview and injured for No Training. | medium | opus |  |
| 0x8b5090 | 8 | `TRAINING_SCHEDULE::set_position_training` | thiscall(TRAINING_SCHEDULE *this, ushort position_bits) returns int, ret 4 | Sets the position training bits of the schedule flags and clears its saved flag. | medium | opus |  |
| 0x8b50c0 | 8 | `TRAINING_SCHEDULE::set_side_training` | thiscall(TRAINING_SCHEDULE *this, ushort side_bits) returns int, ret 4 | Sets the side training bits of the schedule flags and clears its saved flag. | medium | opus |  |
| 0x8b50f0 | 94 | `TRAINING_SCHEDULE::set_default_name` | thiscall(TRAINING_SCHEDULE *this) ret 0 | Writes the default name for the schedule's type into its 11-character name field. | high | opus |  |
| 0x8b5220 | 177 | `TRAINING_SCHEDULE::load_from_file` | thiscall(TRAINING_SCHEDULE *this, const char *path) returns int, ret 4 | Loads a saved training schedule file into this schedule after checking its header magic and version. | high | opus |  |
| 0x8b53d0 | 136 | `TRAINING_SCHEDULE::save_to_file` | thiscall(TRAINING_SCHEDULE *this, const char *path) returns int, ret 4 | Writes this schedule's header, levels, name, type and flags to a training schedule file and marks it saved. | high | opus |  |
| 0x8b5520 | 96 | `training_schedule_get_category_name` | cdecl(char category 0..4, char *out, int out_size) returns int 1 or 0, ret 0 | Writes the name of one of the five training categories into a buffer, or shows an error box for a short buffer or bad category. | high | opus |  |
| 0x8b5690 | 86 | `training_schedule_get_intensity_name` | cdecl(char level 0/10/25/50, char *out, int out_size) returns int 1 or 0, ret 0 | Writes the translated name of a training intensity level into a buffer, or shows a version error box for a short buffer or unknown level. | high | opus |  |
| 0x8b57e0 | 19 | `training_schedule_check_file` | cdecl(const char *path) returns int 1 valid or 2 invalid, ret 0 | Tells the file dialog whether a file is a valid training schedule file by reading its header. | high | opus |  |
| 0x8b5820 | 93 | `training_schedule_read_file_header` | cdecl(const char *path, void *header_out 0x6a bytes) returns bool, ret 0 | Reads the 0x6a-byte header of a training schedule file and returns true when its magic is 0x200cb and its version byte is 1. | high | opus |  |
