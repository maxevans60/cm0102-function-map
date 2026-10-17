# old_international_awards.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x79e580 | 35 (+1 unwind) | `OldInternationalAwards::OldInternationalAwards` | thiscall(OldInternationalAwards* this, FILE* save) ret 4, returns this | Constructs the old-format international awards object with no nation, then loads saved awards or creates fresh ones. | high | opus |  |
| 0x79e5f0 | 205 (+5 unwind) | `OldInternationalAwards::init_awards` | thiscall(OldInternationalAwards* this, FILE* save) ret 4 | Allocates the table of five old international year awards, or reports a failed allocation in an error box. | high | opus |  |
| 0x79e890 | 137 | `OldInternationalAwards::daily_update` | thiscall(OldInternationalAwards* this, Date* today) ret 4 | Outside 2001, fills the first award shortlist on 6 April, gives two player awards on 6 May and three filtered awards on 16 May. | high | opus |  |
