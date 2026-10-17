# denmark_awards.cpp: 5 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x554dc0 | 40 (+1 unwind) | `DenmarkAwards::DenmarkAwards` | thiscall(DenmarkAwards* this, FILE* load_source or 0) ret 4, returns this | Constructs the Danish awards object on NationAwards, sets its nation, and loads the awards from the file or creates them. | high | opus |  |
| 0x554e50 | 337 (+10 unwind) | `DenmarkAwards::init_awards` | thiscall(DenmarkAwards* this, FILE* load_source or 0) ret 4 | Allocates the table of ten Danish awards: one national year award, and for each of three divisions a team award and two year awards. | high | opus |  |
| 0x5552a0 | 151 | `DenmarkAwards::daily_update` | thiscall(DenmarkAwards* this, Date* date) ret 4 | Gives the Danish top player awards on 20 November and each division's player and young player of the year awards on 6 May. | high | opus |  |
| 0x555430 | 14 | `DenmarkAwards::update_team_of_the_week` | thiscall(DenmarkAwards* this, TEAM_AWARD* award) ret 4 | Builds the team of the week for an award when it is one of the three Danish divisional team awards. | high | opus |  |
| 0x555460 | 21 | `DENMARK_RULES::DENMARK_RULES` | thiscall(DENMARK_RULES* this, u8 flag, int nation_index, int continent_index, int arg4, int arg5) ret 0x14, returns this | Constructs the Danish transfer rules on TRANSFER_RULES with no transfer window records, so Danish clubs can sign players at any time. | high | opus | 2026-10-16-sweep-rulebooks.md, 2026-10-16-sweep-season-end.md |
