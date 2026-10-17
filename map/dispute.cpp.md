# dispute.cpp: 11 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x5697e0 | 72 (+2 unwind) | `DISPUTE::DISPUTE` | thiscall(DISPUTE* this, zip_handle saved_game or 0) ret 4, returns this | Constructs the dispute object, loading dispute.dat from a saved game or else creating an empty flag buffer and an empty dispute list. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x5698d0 | 22 | `DISPUTE::~DISPUTE` | thiscall(DISPUTE* this) ret 0 | Frees the dispute flag buffer and destroys the dispute list of the dispute object. | high | opus |  |
| 0x569910 | 150 (+2 unwind) | `DISPUTE::load` | thiscall(DISPUTE* this, zip_handle saved_game) ret 4, returns bool | Reads dispute.dat from a saved game into the dispute object, first the flag buffer and then the list of 17-byte dispute records. | high | opus |  |
| 0x569ae0 | 262 | `DISPUTE::save` | thiscall(DISPUTE* this, zip_handle saved_game) ret 4, returns bool | Writes the dispute flag buffer and the list of 17-byte dispute records to dispute.dat in a saved game, showing an error box on failure. | high | opus |  |
| 0x569e30 | 65 | `DISPUTE::is_in_dispute` | thiscall(DISPUTE* this, Staff* staff, int skip_contract_check) ret 8, returns bool | Returns the staff member's dispute flag and drops the dispute when the FIFA rules are off or the player has no contract or club. | medium | opus |  |
| 0x569ed0 | 119 | `DISPUTE::process_hearings` | thiscall(DISPUTE* this) ret 0 | Resolves each due dispute in the list, releasing the player on a free transfer or keeping him at his club, and posts the outcome news. | medium | opus |  |
| 0x56a030 | 44 | `DISPUTE::get_dispute_club_id` | thiscall(DISPUTE* this, Staff* staff) ret 4, returns int | Returns the club id stored in the staff member's dispute entry, or -1 when the staff member has no dispute. | medium | opus |  |
| 0x56a090 | 47 | `DISPUTE::remove_dispute` | thiscall(DISPUTE* this, Staff* staff) ret 4 | Clears the staff member's dispute flag and removes his entry from the dispute list. | high | opus |  |
| 0x56a100 | 205 (+2 unwind) | `DISPUTE::file_complaint` | thiscall(DISPUTE* this, Staff* staff, Club* club, char reason_a, char reason_b) ret 0x10 | Starts a Player Status Committee complaint, setting dislikes and reputations, queuing a hearing 2 to 21 days ahead and posting the complaint news. | medium | opus |  |
| 0x56a3b0 | 125 (+1 unwind) | `dispute_post_news` | stdcall(Staff* staff, Club* club, char outcome, char reason_a, char reason_b) ret 0x14 | Builds a dispute news item for a player and club and sends it to his nation managers, or to all managers for a famous player. | high | opus |  |
| 0x56a560 | 398 | `dispute_write_news_text` | stdcall(NewsItem* item, int part, int arg) ret 0xc | Writes the headline or body text of a dispute news item, choosing the wording from the outcome code in slot 9. | high | opus |  |
