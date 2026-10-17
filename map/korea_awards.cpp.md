# korea_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x66e030 | 82 (+2 unwind) | `KoreaAwards::KoreaAwards` | thiscall(KoreaAwards* this, FILE* file or 0) ret 4, returns this | Constructs the Korean awards on NationAwards, sets its nation record, then loads the awards from the file or creates the month ratings and award table. | high | opus |  |
| 0x66e170 | 260 (+7 unwind) | `KoreaAwards::init_awards` | thiscall(KoreaAwards* this, FILE* file or 0) ret 4 | Allocates the table of seven Korean awards and creates one team award, one month award and five year awards. | high | opus |  |
| 0x66e4d0 | 118 | `KoreaAwards::daily_update` | thiscall(KoreaAwards* this, Date* date) ret 4 | On day 26 of month index 10, gives the Korean year awards, advances the month award slots, then runs the base update. | high | opus |  |
| 0x66e610 | 7 | `KoreaAwards::on_month_change` | thiscall(KoreaAwards* this) ret 0 | Gives the Korean player of the month award from the month ratings object. | high | opus |  |
