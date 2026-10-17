# os.cpp: 4 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7a16d0 | 17 | `os_get_total_physical_memory_mb` | cdecl(void) ret 0, returns int | Returns the total physical memory of the machine in megabytes from GlobalMemoryStatus. | high | opus | 2026-10-14-import-inventory.md, kernel32.c |
| 0x7a1710 | 16 | `os_get_free_memory_mb` | cdecl(void) ret 0, returns unsigned int | Returns the free physical memory plus free page file in megabytes for the game's memory checks. | high | opus | 2026-10-14-game-creation-inventory.md, 2026-10-14-import-inventory.md, 2026-10-14-select-leagues-spec.md, 2026-10-14-start-new-game-inventory.md, kernel32.c, setup.c |
| 0x7a1750 | 72 | `os_get_cpu_speed_class` | cdecl(void) ret 0, returns int speed class | Reads the CPU speed from cpuinf32.dll, falls back to 150 MHz, and returns a speed class from 0 for fast to 2 for slow. | high | opus | 2026-10-14-import-inventory.md |
| 0x7a1820 | 172 | `os_get_free_disk_space_mb` | cdecl(LPCSTR path) ret 0, returns unsigned int | Returns the free disk space of a path in megabytes, using GetDiskFreeSpaceA on old Windows 95 and GetDiskFreeSpaceExA otherwise, and 150 on failure. | high | opus | 2026-10-14-game-creation-inventory.md, 2026-10-14-import-inventory.md |
