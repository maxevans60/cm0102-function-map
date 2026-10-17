# rb_europe.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dd400 | 21 | `RbEurope::RbEurope` | thiscall (this, FILE* file), ret 4 | Constructs the European ruling body on the RulingBody base, then sets its vtable, nation and continent ids and ban scale fields. | high | opus |  |
| 0x7dd450 | 98 (+1 unwind) | `RbEurope::process_match_cards` | thiscall (this, Booking* booking, Match* match), ret 8 | Adds a match's bookings to the player's European record, banning one match for a red card and one match per three yellows. | high | opus |  |
| 0x7dd5a0 | 48 | `RbEurope::get_name` | thiscall (this, char* buf, int buf_len, int form), ret 0xc | Writes the European continent adjective into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
