# awol.cpp: 19 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x418440 | 131 (+6 unwind) | `AWOL::AWOL` | thiscall(AWOL* this, zip_dir* load_source or 0) ret 4, returns this | Loads the AWOL state from awol.dat when a save is given, otherwise or on failure creates three empty lists and a per-staff flag table. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x4185f0 | 40 | `AWOL::~AWOL` | thiscall(AWOL* this) ret 0 | Frees the per-staff flag table and destroys the three AWOL record lists, clearing each pointer. | high | opus |  |
| 0x418670 | 266 (+6 unwind) | `AWOL::load` | thiscall(AWOL* this, zip_dir* dir) ret 4, returns 1 on success | Reads awol.dat from a save: the per-staff flag table, the absence list, the missed training list and, for newer saves, the fitness incident list. | high | opus |  |
| 0x418980 | 460 | `AWOL::save` | thiscall(AWOL* this, zip_dir* dir) ret 4, returns 1 on success | Writes awol.dat to a save: the staff count, the per-staff flag table and the three AWOL record lists. | high | opus |  |
| 0x418f60 | 55 | `AWOL::is_player_awol` | thiscall(AWOL* this, Staff* staff, int skip_check) ret 8, returns bool in AL | Tests the AWOL bit for a staff member and, unless told to skip, removes the entry when the person has no contracted club. | high | sonnet |  |
| 0x418ff0 | 46 | `AWOL::has_missed_training` | thiscall(AWOL* this, Staff* staff) ret 4, returns bool | Tests the missed training bit of a staff member and drops the record first when the person no longer has a contracted club. | medium | opus |  |
| 0x419070 | 42 | `AWOL::has_fitness_incident` | thiscall(AWOL* this, Staff* staff) ret 4, returns bool | Returns true when the staff member has a record in the recent fitness incident list. | medium | opus |  |
| 0x4190d0 | 505 | `AWOL::daily_update` | thiscall(AWOL* this) ret 0 | Returns one player whose absence ends, resolves a missed training case after a week and expires fitness incidents, adjusting professionalism and temperament. | medium | opus |  |
| 0x4196a0 | 52 | `AWOL::clear_awol` | thiscall(AWOL* this, Staff* staff) ret 4 | Clears the AWOL bit of a staff member and removes his record from the absence list. | high | opus |  |
| 0x419710 | 58 | `AWOL::end_absence` | thiscall(AWOL* this, awol_record* record) ret 4 | Ends a player's absence by posting the return news when he has a club, clearing his AWOL bit and removing the record. | high | opus |  |
| 0x4197c0 | 52 | `AWOL::clear_missed_training` | thiscall(AWOL* this, Staff* staff) ret 4 | Clears the missed training bit of a staff member and removes his record from the missed training list. | high | opus |  |
| 0x419840 | 206 (+2 unwind) | `AWOL::start_absence` | thiscall(AWOL* this, Staff* player, Club* club or 0, char reason: 1 denied move, 4 leave, else general) ret 0xc | Sends a player AWOL, cuts his reputations, adds dislikes with club staff and squad, schedules his return date and posts the news. | high | opus |  |
| 0x419ad0 | 120 (+1 unwind) | `awol_post_news` | stdcall(Staff* player, Club* club, char kind, short arg) ret 0x10 | Posts the AWOL news item for a player, to the managers of his nations or to all managers when his world reputation is high. | high | opus |  |
| 0x419c60 | 554 | `write_awol_news_text` | stdcall(NewsItem* item, int full_text, Text* out) ret 0xc | Writes the headline or body of the AWOL news, choosing return, refusal, denied move or failed to return from leave wording by kind. | high | opus |  |
| 0x41a360 | 233 (+1 unwind) | `AWOL::miss_training` | thiscall(AWOL* this, Staff* player) ret 4 | Sends a very unhappy player AWOL, or else marks him as missing training, posts the coach report, lowers his fitness and may fine him. | medium | opus |  |
| 0x41a630 | 207 (+1 unwind) | `awol_post_missed_training_news` | stdcall(Staff* player, Club* club) ret 8 | Posts the news that a player missed training, reported by the club's head coach or another coach, to the human manager or the nation's managers. | high | opus |  |
| 0x41a8e0 | 399 | `write_missed_training_news_text` | stdcall(NewsItem* item, int full_text, Text* out) ret 0xc | Writes the headline or body of the missed training news, including the manager fining the player or the board losing patience. | high | opus |  |
| 0x41add0 | 185 (+2 unwind) | `AWOL::report_poor_fitness` | thiscall(AWOL* this, Staff* player, Club* club) ret 8 | Records a fitness incident for a player, posts the fitness worry news to a human manager with a random coach and may fine the player. | medium | opus |  |
| 0x41b030 | 295 | `write_fitness_worry_news_text` | stdcall(NewsItem* item, int full_text, Text* out) ret 0xc | Writes the headline or body of the news that a coach worries about a player's fitness after he arrived late for training. | high | opus |  |
