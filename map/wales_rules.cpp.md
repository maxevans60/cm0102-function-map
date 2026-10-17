# wales_rules.cpp: 2 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x90f080 | 79 (+1 unwind) | `WALES_RULES::WALES_RULES` | thiscall(WALES_RULES* this, 5 args forwarded to TRANSFER_RULES::TRANSFER_RULES) ret 0x14 | Constructs the Wales transfer rules, sets vtable 0x970a9c and allocates and fills the 12-byte transfer window table. | high | opus | 2026-10-16-sweep-rulebooks.md |
| 0x90f1a0 | 38 | `WALES_RULES::get_loan_period` | thiscall(WALES_RULES* this, int nation, int unused, char* out_month, short* out_year, char* out_stamp_month, short* out_stamp_year, int unused) ret 0x1c | Returns next month and year from today, then replaces them with the nation's contract date month and the year in which it next falls. | high | opus |  |
