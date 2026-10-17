# match_official.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6e9460 | 4 | `MATCH_OFFICIAL::MATCH_OFFICIAL` | thiscall(MATCH_OFFICIAL* this) ret 0, returns this | Constructs the match referee object by clearing its engine and official pointers. | high | opus |  |
| 0x6e9470 | 67 | `MATCH_OFFICIAL::init` | thiscall(MATCH_OFFICIAL* this, CM3_MATCH_ENGINE* engine, Official* official or null) ret 8 | Stores the engine and the match official and sets the referee's starting leniency score from his current ability, with random draws. | high | opus |  |
| 0x6e9540 | 96 | `MATCH_OFFICIAL::check_foul` | thiscall(MATCH_OFFICIAL* this, MATCH_PLAYER* player, short action_code, uint8* out_kind, char* out_severity) ret 0x10, returns 1 when a foul is given | Decides whether the referee gives a foul against a player and writes the result code and a severity from the player's fouls. | medium | opus |  |
| 0x6e9630 | 164 | `MATCH_OFFICIAL::decide_booking` | thiscall(MATCH_OFFICIAL* this, MATCH_PLAYER* player, char* outcome, char reason, char severity, char in_box, float* out_weight) ret 0x18 | Counts a foul for the player and his side and decides whether he gets a yellow card, a second yellow or a red card. | medium | opus |  |
| 0x6e9820 | 941 | `MATCH_OFFICIAL::judge_tackle` | thiscall(MATCH_OFFICIAL* this, MATCH_PLAYER* offender, MATCH_PLAYER* victim, int action_code, char context, uint8* out_kind, char* out_severity, char* out_hurt) ret 0x1c, returns char | Judges a challenge by its action code and decides whether the referee calls a foul, how serious it is and whether the victim is hurt. | medium | opus |  |
| 0x6ea4e0 | 184 | `MATCH_OFFICIAL::decide_foul_punishment` | thiscall(MATCH_OFFICIAL* this, MATCH_PLAYER* offender, MATCH_PLAYER* victim, char* outcome, char reason, char severity, char serious, float* out_weight, char flag_0x16) ret 0x20 | Counts a foul for the offender and the victim and decides whether the offender gets a yellow card, a second yellow or a red card. | medium | opus |  |
| 0x6ea760 | 294 | `MATCH_OFFICIAL::find_offside_player` | thiscall(MATCH_OFFICIAL* this, char attacking_side, char ball_row, char target_row, MATCH_PLAYER* receiver) ret 0x10, returns MATCH_PLAYER* or 0 | Looks for an attacker beyond the offside line and decides whether the official flags him, adjusting the official's decision score. | medium | opus |  |
| 0x6eab60 | 208 | `MATCH_OFFICIAL::decide_card` | thiscall(MATCH_OFFICIAL* this, MATCH_PLAYER* offender, char* out_decision, char offence_type, char no_record) ret 0x10 | Decides whether a foul earns no card, a booking, a second booking or a red card, and records the offence on the player. | high | opus | 2026-10-14-violent-conduct-inventory.md |
