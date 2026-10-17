# rb_denmark.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dcae0 | 25 | `RbDenmark::RbDenmark` | thiscall (this, FILE* file), ret 4 | Constructs the Danish ruling body on the RulingBody base, then sets its vtable, nation and continent ids and ban scale fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dcb30 | 231 (+4 unwind) | `RbDenmark::process_match_cards` | thiscall (this, Booking* booking, Match* match), ret 8 | Adds disciplinary points for a match's yellow and red cards to the player's Danish record and bans the player when a points threshold is crossed. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dce70 | 47 | `RbDenmark::get_name` | thiscall (this, char* buf, int buf_len, int form), ret 0xc | Writes the Danish nationality adjective into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7dcf30 | 33 | `RbDenmark::is_one_booking_from_ban` | thiscall (this, DisciplineEntry* entry, char* out_flag, char* out_rule_set, int comp_id), ret 0x10 | Reports whether three more disciplinary points take the player's Danish points total to or past the next ban threshold. | high | opus | 2026-10-16-sweep-rulebooks.md |
