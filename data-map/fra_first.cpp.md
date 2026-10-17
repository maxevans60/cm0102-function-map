# fra_first.cpp: 3 globals owned by fra_first.cpp

Data map of cm0102.exe 3.9.68: the globals that game and library functions touch. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

A global is high only when the evidence quotes a string, an assert, a constant in read-only data, or a high function whose name pins the purpose. Treat a medium or low name as a hint. Fields of an address group are described as `g_<object>+0x<offset> <field>`. Readers and writers link to the function map. "Cited in" lists research docs and runtime files of the Bosman Edition repo that name the address.

| Address | Size | Type | Name | Description | Evidence | Confidence | Model | Writers | Readers | Cited in |
|---|---|---|---|---|---|---|---|---|---|---|
| 0x96a904 | 144 | vtable | `g_vtable_fra_lower_stub_comp` | The vtable of the FraLowerStubComp competition object. | Stored into the object by 0x5bb160 FraFirst::FraFirst and by the member 0x5bb5b0 FraLowerStubComp::~FraLowerStubComp, which takes the object in ECX. | high | sonnet |  | [0x5bb160](../map/fra_first.cpp.md), [0x5bb5b0](../map/fra_first.cpp.md) |  |
| 0x96a994 | 144 | vtable | `g_vtable_fra_cfa_stub_comp` | The vtable of the FraCfaStubComp competition object. | Stored into the object by 0x5bb160 FraFirst::FraFirst and by the member 0x5bb580 FraCfaStubComp::~FraCfaStubComp, which takes the object in ECX. | high | sonnet |  | [0x5bb160](../map/fra_first.cpp.md), [0x5bb580](../map/fra_first.cpp.md) |  |
| 0x96aa24 | 180 | vtable | `g_vtable_fra_first` | Vtable of FraFirst, 45 slots. | the destructor or constructor of FraFirst holds it: 0x5bb160 FraFirst::FraFirst, 0x5bb5e0 FraFirst::~FraFirst | high | script |  | [0x5bb160](../map/fra_first.cpp.md), [0x5bb5e0](../map/fra_first.cpp.md) |  |
