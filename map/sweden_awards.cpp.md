# sweden_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x893720 | 40 (+1 unwind) | `SwedenAwards::SwedenAwards` | thiscall(SwedenAwards* this, int load_source), ret 4 | Runs the NationAwards constructor, installs vtable 0x970354, then loads the awards from the save or builds them fresh with init_awards. | high | opus |  |
| 0x8937b0 | 332 (+10 unwind) | `SwedenAwards::init_awards` | thiscall(SwedenAwards* this, int load_source), ret 4 | Allocates the ten-entry award array and builds the Swedish year and team awards, with an error box when allocation fails. | high | opus |  |
| 0x893bf0 | 141 | `SwedenAwards::daily_update` | thiscall(SwedenAwards* this, Date* today), ret 4 | Hands out the Swedish manager and player of the year awards on the season award date, then runs the base daily update. | high | opus |  |
| 0x893d60 | 12 | `SwedenAwards::update_team_of_the_week` | thiscall(SwedenAwards* this, Award* award), ret 4 | Builds the team of the week when the given award is one of the two Swedish team awards. | high | opus |  |
| 0x893d80 | 22 | `SWEDEN_RULES::SWEDEN_RULES` | thiscall(SWEDEN_RULES* this, int a1, int a2, int a3, int a4, int rules_id), ret 0x14 | Runs the TRANSFER_RULES constructor and installs the Swedish rules vtable 0x970368 with no transfer window records. | high | opus | 2026-10-16-sweep-rulebooks.md |
