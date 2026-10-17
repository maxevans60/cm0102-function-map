# international_awards.cpp: 3 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x632ac0 | 35 (+1 unwind) | `InternationalAwards::InternationalAwards` | thiscall(InternationalAwards* this, FILE* load_source or 0), ret 4, returns this | Constructs the international awards object on NationAwards with no nation record, then loads saved awards or creates the award table. | high | opus |  |
| 0x632b30 | 233 (+6 unwind) | `InternationalAwards::init_awards` | thiscall(InternationalAwards* this, FILE* load_source or 0), ret 4 | Allocates the table of six international awards and creates each one as a year award with no competition. | high | opus |  |
| 0x632e20 | 149 | `InternationalAwards::daily_update` | thiscall(InternationalAwards* this, Date* date), ret 4 | Outside 2001, gives the world player awards on two fixed dates and the four continental player awards on day 16 of month index 5. | high | opus |  |
