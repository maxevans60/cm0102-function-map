# rb_finland_cup.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dd660 | 22 | `RbFinlandCup::RbFinlandCup` | thiscall (this, FILE* file), ret 4 | Constructs the Finnish cup ruling body on the RulingBody base, then sets its vtable, nation and continent ids and ban scale fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dd6b0 | 153 (+4 unwind) | `RbFinlandCup::process_match_cards` | thiscall (this, Booking* booking, Match* match), ret 8 | Adds a match's bookings to the player's Finnish cup record, banning per three yellows and queueing a red card points ban one week later. | high | opus |  |
| 0x7dd8f0 | 38 | `RbFinlandCup::get_name` | thiscall (this, char* buf, int buf_len, int form), ret 0xc | Writes "Finnish cup" into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
