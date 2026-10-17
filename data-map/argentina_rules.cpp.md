# argentina_rules.cpp: 1 globals owned by argentina_rules.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x9674a0 | 52 | vtable | `g_vtable_argentina_rules` | The vtable of the ArgentinaRules competition object. | Stored at the start of the object by the constructor 0x40a580 ARGENTINA_RULES::Argentina_rules, its only reader. Next global starts 52 bytes later. | high | sonnet |  | [0x40a580](../map/argentina_rules.cpp.md) |  |
