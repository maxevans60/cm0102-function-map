# zipdir.cpp: 10 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x9326e0 | 348 | `zopen` | cdecl (const char *archive_path, const char *member_name, int write_mode, int header_arg, int header_type), returns ZFILE * or NULL | Opens a named member inside a game archive file for reading or adds a new member for writing. | high | opus | 2026-10-15-attribute-groups.md, testrun.c |
| 0x932b00 | 101 | `zclose` | cdecl (ZFILE **handle) | Closes an archive member handle, flushing pending compressed output and the directory when writing, then frees it. | high | opus | 2026-10-15-attribute-groups.md, testrun.c |
| 0x932c30 | 169 | `zread` | cdecl (void *buffer, int size, int count, ZFILE *zf), returns items read | Reads items from an archive member like fread, decoding run length compressed data when the archive type is 4. | high | opus | 2026-10-13-database-inventory.md, 2026-10-14-start-new-game-inventory.md, 2026-10-15-commentary-speed-inventory.md, 2026-10-15-holiday-next-match-inventory.md |
| 0x932e10 | 190 | `zwrite` | cdecl (const void *buffer, int size, int count, ZFILE *zf), returns count | Writes items to an archive member like fwrite, run length encoding the data when the archive type is 4. | high | opus | 2026-10-15-attribute-groups.md, 2026-10-15-commentary-speed-inventory.md, testrun.c |
| 0x933080 | 101 | `zseek` | cdecl(ZFILE *zf, int offset, int origin 0 start, 1 current, 2 end) returns int 0 or -1, ret 0 | Seeks inside an archive member like fseek, rejecting positions outside the member and replaying reads for run length compressed members. | high | opus |  |
| 0x933170 | 32 | `ztell` | cdecl(ZFILE *zf) returns int position or -1, ret 0 | Returns the current position inside an archive member like ftell. | high | opus |  |
| 0x9331c0 | 113 | `zget_archive_id` | cdecl(const char *archive_path) returns int archive id, 0x14 on failure, ret 0 | Reads the header of a game archive file and returns its archive id field, or 0x14 when the file is missing or invalid. | high | opus |  |
| 0x933320 | 233 | `zextract_matching_files` | cdecl(const char *archive_path, const char *dest_folder, const char *pattern) returns int 1 if any file was extracted, ret 0 | Extracts each archive member whose name matches a pattern into files in a folder. | high | opus |  |
| 0x933610 | 173 | `zadd_matching_files` | cdecl(const char *archive_path, const char *src_folder, const char *pattern, int header_arg, int header_type) returns int 1 or 0, ret 0 | Adds every file in a folder that matches a pattern to an archive as a new member. | high | opus |  |
| 0x933860 | 141 | `zget_matching_size` | cdecl(const char *archive_path, const char *pattern) returns int total bytes, 0 on failure, ret 0 | Returns the sum of the stored lengths of the archive members whose names match a pattern. | high | opus |  |
