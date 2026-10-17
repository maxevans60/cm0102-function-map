# eng_prm.cpp: 2 globals owned by eng_prm.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x969d1c | 180 | vtable | `g_vtable_eng_prm` | Vtable of EngPrm, 45 slots. | the destructor or constructor of EngPrm holds it: 0x573380 EngPrm::EngPrm, 0x5735d0 EngPrm::~EngPrm | high | script |  | [0x573380](../map/eng_prm.cpp.md), [0x5735d0](../map/eng_prm.cpp.md) |  |
| 0xb71b00 | 0 | unknown | `g_not_a_global_const_12000000` | Not a global. The value 0xb71b00 is the number 12,000,000 used as an immediate prize money amount. | EngPrm::create_table 0x574a20 picks 5,000,000 (0x4c4b40) before year 2000 and this value after, as the amount for 0x683010 League::pay_clubs. 0x85e960 only compares a register with it. | high | sonnet |  | [0x574a20](../map/eng_prm.cpp.md), [0x85e960](../map/staff_contracts.cpp.md) |  |
