# asia_cup_winner.cpp: 2 globals owned by asia_cup_winner.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x967574 | 160 | vtable | `g_vtable_asia_cup_winner` | Vtable of AsiaCupWinner, 40 slots. | the destructor or constructor of AsiaCupWinner holds it: 0x40cbe0 AsiaCupWinner::AsiaCupWinner, 0x40ce70 AsiaCupWinner::~AsiaCupWinner | high | script |  | [0x40cbe0](../map/asia_cup_winner.cpp.md), [0x40ce70](../map/asia_cup_winner.cpp.md) | 2026-10-16-sweep-europe.md |
| 0xad9c5c | 4 | void * | `g_asia_club_championship_comp_cache` | Cached pointer to the Asian Club Championship competition, found on first use. | 0x40e7b0 asia_cup_winner_club_in_club_championship searches the competition table once and keeps the result here. It is medium because the name of the function is medium. | medium | sonnet | [0x40e7b0](../map/asia_cup_winner.cpp.md) | [0x40e7b0](../map/asia_cup_winner.cpp.md) |  |
