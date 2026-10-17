# cash.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x43f2d0 | 18 | `swap_bytes_16_array` | cdecl (u16 *words, int count) ret 0 | Reverses the byte order of each 16-bit word in a buffer in place. | high | opus |  |
| 0x43f300 | 29 | `swap_bytes_32_array` | cdecl (u32 *words, int count) ret 0 | Reverses the byte order of each 32-bit word in a buffer in place. | high | opus |  |
| 0x43f350 | 79 | `swap_bytes_64_array` | cdecl (u64 *qwords, int count) ret 0 | Reverses the byte order of each 64-bit word in a buffer in place. | medium | opus |  |
| 0x43f440 | 10 | `cash_currency_prefix_length` | cdecl (void) ret 0, returns length in EAX | Returns the length of the current currency prefix string at 0xad9ca8. | high | opus |  |
| 0x43f460 | 46 | `Cash::get_display_amount` | thiscall(const Cash* this, uint flags), ret 4, returns int64 in EDX:EAX | Converts the stored amount to the chosen currency with the rate at 0xad9cb8 and rounds it to the display step unless flag 0x20 asks for the exact value. | high | opus |  |
| 0x43f4c0 | 8 | `Cash::set_from_display` | thiscall (Cash *this, s64 display_amount) ret 8 | Stores a display currency amount in the cash value by dividing it by the currency rate. | high | opus |  |
| 0x43f4e0 | 66 | `Cash::step_up` | thiscall (Cash *this, u32 flags) ret 4 | Raises the cash value to the next rounding step of its display currency amount, rounding to the step first unless flag 0x20 is set. | high | opus | 2026-10-16-slow-screens.md |
| 0x43f580 | 62 | `Cash::step_down` | thiscall (Cash *this, u32 flags) ret 4 | Lowers the cash value by one rounding step of its display currency amount, rounding to the step first unless flag 0x20 is set. | high | opus | 2026-10-16-slow-screens.md |
| 0x43f620 | 68 | `Cash::set_from_preset_index` | thiscall(Cash* this, char preset_index) ret 4, returns the stored value | Stores one of seven preset money amounts, from 100,000 to 10,000,000, as a cash value in the current currency, or asserts on a bad index. | high | opus |  |
| 0x43f720 | 54 | `Cash::set_from_amount_table` | thiscall(Cash* this, char index, const int* amounts, short count) ret 0xc, returns the stored value | Stores the amount at an index of a caller table as a cash value, or asserts on a null table or bad index. | high | opus |  |
| 0x43f7f0 | 2327 | `cash_set_currency` | cdecl(char currency_id) ret 0, returns 1 or 0 | Sets the active currency: exchange rate, scale factors, unit suffixes for thousands, millions and billions, separators, and the current currency id. | high | opus |  |
| 0x4415e0 | 2 | `cash_get_currency` | cdecl(void) ret 0, returns char currency id | Returns the id of the active currency. | high | opus |  |
| 0x4415f0 | 552 | `cash_get_currency_name` | cdecl(char* buffer, short buffer_size, char currency_id) ret 0, returns 1 or 0 | Copies the short name of a currency, such as Peso, Aus$ or Pta, into a buffer of at least 50 characters. | high | opus |  |
| 0x441c10 | 805 | `cash_format_money` | cdecl(char* buffer, short size, int64 amount, byte flags) ret 0, returns int | Writes a 64-bit money amount as text with the currency prefix and suffix, adding thousands separators when flag 2 is set. | high | opus |  |
| 0x442070 | 31 | `cash_format_money_fragment_442070` | not a function: a mid-instruction address inside cash_format_money | Marks a false entry point inside one switch case of cash_format_money that writes a ten-digit amount with separators. | high | opus |  |
| 0x4426e0 | 272 | `cash_get_rounding_step` | cdecl(int64 amount, byte flags) ret 0, returns int step | Returns the rounding step for a money amount from a threshold ladder chosen by flag 4 or 8, or 1000 without either flag. | high | opus |  |
