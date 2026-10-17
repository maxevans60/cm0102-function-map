# comp_text.cpp: 8 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x4ae590 | 12 | `Text::Text` | thiscall(Text* this, const char* initial) ret 4, returns this | Constructs a text object with no string and no link list, copying the initial string when one is given. | high | opus | 2026-10-16-comparison-screen-inventory.md |
| 0x4ae5c0 | 37 | `Text::Text` | thiscall(Text* this, const Text* src) ret 4, returns this | Constructs a text object as a copy of another, copying its string and adding each of its links. | high | opus |  |
| 0x4ae630 | 18 | `Text::~Text` | thiscall(Text* this) ret 0 | Frees the string and the link list of a text object. | high | opus | 2026-10-16-comparison-screen-inventory.md |
| 0x4ae660 | 92 | `Text::set_string` | thiscall(Text* this, const char* source) ret 4, returns int | Replaces the string of a text object with a newly allocated copy of the source string. | high | opus | 2026-10-14-clickable-names-inventory.md, 2026-10-16-comparison-screen-inventory.md |
| 0x4ae770 | 100 | `Text::append_string` | thiscall(Text* this, const char* source) ret 4, returns int | Appends a string to the string of a text object, or sets it when the object is empty. | high | opus |  |
| 0x4ae8a0 | 174 (+1 unwind) | `Text::add_link` | thiscall(Text* this, const char* phrase, int link_type, void* target) ret 0xc, returns int | Adds a hyperlink for a phrase in the text to the link list, unless the phrase is already linked. | high | opus | 2026-10-14-clickable-names-inventory.md, 2026-10-16-comparison-screen-inventory.md, 2026-10-16-sweep-season-end.md |
| 0x4aeaf0 | 954 | `Text::draw_wrapped` | thiscall(Text* this, short slot, int left, int right, int* line, short font, short colour, ushort style, byte flags) ret 0x20, returns int | Splits the text into lines that fit between two x positions and adds display entries for each line and its linked phrases. | medium | opus | 2026-10-14-clickable-names-inventory.md, 2026-10-14-start-screen-spec.md, 2026-10-14-widescreen-inventory.md, 2026-10-15-attribute-groups.md, 2026-10-16-comparison-screen-inventory.md, 2026-10-16-crash-fixes.md, build-brief-0.5.0.md, display.c, gui_menu.c, names.c |
| 0x4afa40 | 23 | `Text::clear` | thiscall(Text* this) ret 0, returns 1 | Frees the string and link list of a text object and sets both pointers to null so the object can be reused. | high | opus | 2026-10-16-comparison-screen-inventory.md |
