# rb_england.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7dcf90 | 34 (+1 unwind) | `RbEngland::RbEngland` | thiscall (this, FILE* file), ret 4 | Constructs the English ruling body on the RulingBody base, then sets its vtable, nation and continent ids and ban scale fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7dd010 | 234 (+6 unwind) | `RbEngland::process_match_cards` | thiscall (this, Booking* booking, Match* match), ret 8 | Applies English yellow card totals with seasonal cut off dates and red card bans by offence type, adding a ban that starts fourteen days later. | high | opus |  |
| 0x7dd2e0 | 47 | `RbEngland::get_name` | thiscall (this, char* buf, int buf_len, int form), ret 0xc | Writes the English nationality adjective into the buffer as its name, or shows a version error box when the buffer is under 20 bytes. | high | opus |  |
| 0x7dd3a0 | 31 | `RbEngland::is_one_booking_from_ban` | thiscall (this, DisciplineEntry* entry, char* out_flag, char* out_rule_set, int comp_id), ret 0x10 | Reports whether the next yellow card is a fifth, tenth, fifteenth or twentieth, and ignores the fifth between days 101 and 170. | high | opus | 2026-10-16-sweep-rulebooks.md |
