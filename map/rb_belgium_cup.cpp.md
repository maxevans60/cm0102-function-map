# rb_belgium_cup.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7db8f0 | 22 | `RbBelgiumCup::RbBelgiumCup` | thiscall(RbBelgiumCup* this, FILE* file) returning this, ret 4 | Constructs the Belgian cup ruling body on the RulingBody base, sets vtable 0x96ea54, rule set id 5 and the Belgium nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7db940 | 194 (+4 unwind) | `RbBelgiumCup::process_match_cards` | thiscall(RbBelgiumCup* this unused, PlayerMatchRecord* rec, Fixture* fixture) returning uint, ret 8 | Applies a player's match cards under Belgian cup rules, queueing a points ban for a red card and banning him at each third booking. | high | opus |  |
| 0x7dbc00 | 38 | `RbBelgiumCup::get_name` | thiscall(RbBelgiumCup* this unused, char* buf, int buf_len, int form) ret 0xc | Writes Belgian cup into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
