# training_edit_session.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8b0a00 | 76 (+2 unwind) | `TRAINING_EDIT_SESSION::TRAINING_EDIT_SESSION` | thiscall(TRAINING_EDIT_SESSION* this, Club* club) ret 4, returns this | Builds an edit session for a club with copies of its ten training schedules, its player groups and its coach record. | high | opus |  |
| 0x8b0b20 | 7 | `TRAINING_EDIT_SESSION::destroy_schedule_slots` | thiscall(TRAINING_EDIT_SESSION* this) ret 0 | Destroys the eleven schedule objects of an edit session during exception unwinding. | high | opus |  |
| 0x8b0b40 | 57 | `TRAINING_EDIT_SESSION::apply_changes` | thiscall(TRAINING_EDIT_SESSION* this) ret 0, returns 1 | Copies the edited schedules, player groups and coach record of the session back to the training manager. | high | opus |  |
| 0x8b0bf0 | 38 | `TRAINING_EDIT_SESSION::select_schedule` | thiscall(TRAINING_EDIT_SESSION* this, char index) ret 4, returns 1 or 0 | Selects one of the ten schedules of the session for editing, or shows an error box for an index outside 0 to 9. | high | opus |  |
| 0x8b0c90 | 21 | `TRAINING_EDIT_SESSION::set_current_schedule` | thiscall(TRAINING_EDIT_SESSION* this, TRAINING_SCHEDULE* source) ret 4 | Copies a schedule into the selected slot of the session and marks that slot and the session as changed. | high | opus |  |
| 0x8b0ce0 | 12 | `TRAINING_EDIT_SESSION::set_coach_record` | thiscall(TRAINING_EDIT_SESSION* this, const void* record 54 bytes) ret 4 | Copies an edited 54-byte coach assignment table into the session and marks the session as changed. | high | opus |  |
| 0x8b0d10 | 22 | `TRAINING_EDIT_SESSION::count_schedule_players` | thiscall(TRAINING_EDIT_SESSION* this, char index or -1 for the selected one) ret 4, returns count | Counts the session players that the chosen schedule applies to, using the selected schedule when the index is -1. | high | opus |  |
| 0x8b0d60 | 31 | `TRAINING_EDIT_SESSION::list_schedule_players` | thiscall(TRAINING_EDIT_SESSION* this, LLIST** out_list or 0, int extra) ret 8 | Fills the session list with the players of the selected schedule, returns the list and stores their count at +0x818. | high | opus |  |
| 0x8b0dc0 | 25 | `TRAINING_EDIT_SESSION::set_player_group` | thiscall(TRAINING_EDIT_SESSION* this, int player, char group) ret 8 | Finds a player among the fifty session entries, stores his new training group and marks the session as changed. | high | opus |  |
| 0x8b0e00 | 29 | `TRAINING_EDIT_SESSION::load_schedule_file` | thiscall(TRAINING_EDIT_SESSION* this, const char* path) ret 4, returns 1 or 0 | Loads a schedule file into the selected slot, marks it as changed and adds the file to the human manager's recent files. | high | opus |  |
| 0x8b0e70 | 22 | `TRAINING_EDIT_SESSION::save_schedule_file` | thiscall(TRAINING_EDIT_SESSION* this, const char* path) ret 4, returns 1 or 0 | Saves the selected schedule to a file and adds the file to the human manager's recent files. | high | opus |  |
