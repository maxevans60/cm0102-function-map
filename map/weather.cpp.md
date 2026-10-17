# weather.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x9226c0 | 88 | `Weather::Weather` | thiscall(Weather* this) ret 0, returns this | Waits until a CD drive holds cm0102.exe, prompting 'Insert CD' in a loop, then clears the weather object and loads weather.cfg. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x9227d0 | 18 | `Weather::~Weather` | thiscall(Weather* this) ret 0 | Frees the two weather tables at +0 and +4 and clears both pointers. | high | opus |  |
| 0x922810 | 307 | `Weather::load_config` | thiscall(Weather* this) ret 0 | Reads weather.cfg from the CM3_DATA folder into a table of 0x6e-byte regions and fills a four-byte random weather entry for each city. | high | opus |  |
| 0x922c40 | 84 | `Weather::read_region` | thiscall(Weather* this, FILE* cfg, Region* out) ret 8, returns bool | Reads one weather region line with its id and name, then reads its four seasonal weather lines into the region record. | high | opus |  |
| 0x922d20 | 130 | `Weather::read_region_period` | thiscall(Weather* this, FILE* cfg, RegionPeriod* out) ret 8, returns bool | Parses one weather.cfg period line into a 0x13-byte record of a day value, five wind, five precipitation and seven heat values. | high | opus |  |
| 0x922ee0 | 100 | `Weather::update_city_weather` | thiscall(Weather* this) ret 0 | Rolls new random weather values from 0 to 100 for every city and, one time in ten, a new wind value from 0 to 2. | high | opus | 2026-10-14-game-creation-inventory.md |
| 0x923010 | 273 | `Weather::get_match_weather` | thiscall(Weather* this, u8* out_conditions, Fixture* fixture or 0) ret 8 | Finds the weather region of a fixture's city and fills a four-byte record with wind, precipitation, temperature and city wind for the match date. | medium | opus |  |
| 0x9232c0 | 68 | `Weather::get_temperature` | thiscall(Weather* this unused, char band, Fixture* fixture or 0) ret 8 | Turns a temperature band and the match day into a temperature between -5 and 40 degrees, adjusted for fixtures of type 2. | medium | opus |  |
| 0x9233a0 | 170 | `weather_format_description` | stdcall(char* out, u8* conditions) ret 8 | Writes the weather of a match as text, joining the wind word, the precipitation word and the temperature. | high | opus |  |
| 0x923630 | 278 | `Weather::check_postponement` | thiscall(Weather* this, Fixture* fixture) ret 4, returns result flags | Decides by random rolls on the match weather, stadium capacity and club finances whether a fixture is postponed or abandoned, and returns the reason flags. | medium | opus |  |
| 0x923970 | 195 | `Weather::get_pitch_condition` | thiscall(Weather* this unused, u8* conditions, Fixture* fixture) ret 8 | Chooses the pitch condition flag of a fixture from its precipitation, temperature, stadium capacity and a hash of the fixture. | medium | opus |  |
| 0x923b60 | 63 | `pitch_condition_text` | stdcall(char* out, u8 condition) ret 8 | Writes the text for a pitch condition flag, such as Muddy, Water-logged, Frozen or Hard. | high | opus |  |
| 0x923cc0 | 70 (+1 unwind) | `Weather::post_postponed_news` | thiscall(Weather* this unused, Fixture* fixture, char reason) ret 8 | After the game start date, creates a news item of type 2 for a postponed fixture and sends it to the managers of both clubs. | medium | opus |  |
| 0x923dd0 | 227 | `weather_write_postponed_news_text` | stdcall(void* item, int full_text, int unused) ret 0xc | Writes the headline or the body of the match postponed news story, choosing the body text by the reason bits, and links both clubs. | high | opus |  |
| 0x924050 | 70 (+1 unwind) | `Weather::post_abandoned_news` | thiscall(Weather* this unused, Fixture* fixture, char reason) ret 8 | After the game start date, creates a news item of type 0x2a for an abandoned fixture and sends it to the managers of both clubs. | medium | opus |  |
| 0x924160 | 246 | `weather_write_abandoned_news_text` | stdcall(void* item, int full_text, int unused) ret 0xc | Writes the headline or the body of the match abandoned news story, choosing the body text by the reason bits, and links both clubs. | high | opus |  |
