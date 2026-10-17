# national_teams_screens.cpp: 1 globals owned by national_teams_screens.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0xb77c88 | 4 | u32 | `g_network_join_name_unmatched_flag` | Set to 1 when a join starts and cleared when the typed host name matches a game in the list. | written only by 0x77a9f0 Network::host_or_join_game (high), which also sends the string CM3 LIST SERVER ACK | medium | sonnet | [0x77a9f0](../map/national_teams_screens.cpp.md) |  |  |
