# rb_argentina.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7db100 | 22 | `RbArgentina::RbArgentina` | thiscall(RbArgentina* this, FILE* file) returning this, ret 4 | Constructs the Argentine ruling body on the RulingBody base, sets vtable 0x96e9f4, rule set id 3 and the Argentina nation fields. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x7db150 | 98 (+1 unwind) | `RbArgentina::process_match_cards` | thiscall(RbArgentina* this unused, PlayerMatchRecord* rec, Fixture* fixture) ret 8 | Applies a player's match cards under Argentine rules, banning him after a red card or each fifth booking and posting the ban news. | high | opus |  |
| 0x7db2a0 | 47 | `RbArgentina::get_name` | thiscall(RbArgentina* this unused, char* buf, int buf_len, int form) ret 0xc | Writes the Argentine nationality adjective into the buffer as the ruling body name, or shows a version error when the buffer is shorter than twenty. | high | opus |  |
