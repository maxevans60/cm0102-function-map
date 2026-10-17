# australia_awards.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x412540 | 82 (+2 unwind) | `AustraliaAwards::AustraliaAwards` | thiscall(AustraliaAwards* this, FILE* file) ret 4, returns this | Builds the Australia awards object, loads it from a save file when one is given, or creates its month ratings and award objects. | high | opus |  |
| 0x412680 | 325 (+9 unwind) | `AustraliaAwards::init_awards` | thiscall(AustraliaAwards* this, FILE* file) ret 4 | Allocates the nine-award table and builds one team award, three month awards and five year awards for Australia. | high | opus | 2026-10-14-widescreen-inventory.md |
| 0x412ac0 | 125 | `AustraliaAwards::daily_update` | thiscall(AustraliaAwards* this, Date* date) ret 4 | On day 20 of month index 5, awards the Australian player and manager of the year honours, then checks for a month change. | high | opus |  |
| 0x412c20 | 35 | `AustraliaAwards::on_month_change` | thiscall(AustraliaAwards* this) ret 0 | Gives the Australian manager of the month award and the player and young player of the month awards from the month ratings. | high | opus |  |
