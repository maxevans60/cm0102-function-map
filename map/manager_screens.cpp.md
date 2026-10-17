# manager_screens.cpp: 28 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x6ae1a0 | 79 | `open_manager_stats_screen` | cdecl(void) ret 0 | Opens the Manager Stats screen for the current human manager's nation and sets its nine screen parameters. | high | opus |  |
| 0x6ae2a0 | 2763 (+4 unwind) | `manager_stats_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Manager Stats screen, which lists managers ranked by a chosen statistic with a nation filter and page buttons. | high | opus |  |
| 0x6b05e0 | 340 | `manager_stats_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles a widget on the Manager Stats screen, setting the nation filter or stat key and paging the list by one or ten rows. | high | opus |  |
| 0x6b09d0 | 19 | `manager_stats_screen_close` | cdecl, no arguments, returns void, ret 0 | Frees the Manager Stats screen row buffer and clears its two list parameters when the screen closes. | high | opus |  |
| 0x6b0a10 | 76 | `open_job_information_screen` | cdecl, no arguments, returns void, ret 0 | Opens the Job Information screen and sets its nation parameter to the nation of the human manager's current job. | high | opus |  |
| 0x6b0b10 | 993 | `job_information_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Job Information screen, listing the clubs of a nation with their manager and job security rating. | high | opus |  |
| 0x6b1790 | 164 | `job_information_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles a widget on the Job Information screen, changing the nation and resetting the list or paging up and down. | high | opus |  |
| 0x6b1980 | 24 | `job_information_screen_close` | cdecl, no arguments, returns void, ret 0 | Frees the Job Information row buffer, clears the list parameters and resets the page to one when the screen closes. | high | opus |  |
| 0x6b19d0 | 50 | `open_apply_for_job_screen` | cdecl(club *club), returns void, ret 0 | Opens the confirm screen that asks the human manager to apply for a club's job, or shows a version error for a null club. | high | opus |  |
| 0x6b1a80 | 129 | `apply_for_job_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Please Confirm screen asking whether to apply for the club job, with No and Yes buttons. | high | opus |  |
| 0x6b1c30 | 75 | `apply_for_job_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the apply confirm buttons, closing on No and calling MANAGER_MANAGER::apply_for_job for the human manager on Yes. | high | opus |  |
| 0x6b1d10 | 50 | `open_resign_job_screen` | cdecl(club *club), returns void, ret 0 | Opens the confirm screen that asks the human manager to resign from a club, or shows a version error for a null club. | high | opus |  |
| 0x6b1dc0 | 129 | `resign_job_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Please Confirm screen asking whether to resign as manager of the club, with No and Yes buttons. | high | opus |  |
| 0x6b1f70 | 88 | `resign_job_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the resign confirm buttons, removing the human manager from the club and opening the vacancy on Yes. | high | opus |  |
| 0x6b2080 | 50 | `open_board_confidence_screen` | cdecl(club *club), returns void, ret 0 | Opens the Board Confidence screen for a club, or shows a version error for a null club. | high | opus | 2026-10-16-stadium-research.md |
| 0x6b2130 | 168 | `board_confidence_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Board or F.A. Confidence screen with the board's confidence and squad opinion text and the request buttons. | high | opus | 2026-10-16-stadium-research.md |
| 0x6b2370 | 74 | `board_confidence_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the Board Confidence buttons, opening the board request screen or the F.A. meeting screen for the club. | high | opus | 2026-10-16-stadium-research.md |
| 0x6b2450 | 104 (+1 unwind) | `open_job_offer_screen` | cdecl(staff *manager, int news_id), returns void, ret 0 | Opens the confirm screen for a job offer news item, storing the news id and the offering club, or shows a version error. | high | opus |  |
| 0x6b25e0 | 129 | `job_offer_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Please Confirm screen asking whether to accept the manager position at the offering club. | high | opus |  |
| 0x6b2790 | 97 | `job_offer_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the job offer buttons, marking the news item answered and either rejecting the offer or appointing the human manager. | high | opus |  |
| 0x6b28b0 | 8 | `open_retire_screen` | cdecl, no arguments, returns void, ret 0 | Opens the confirm screen that asks the human manager to retire from football. | high | opus |  |
| 0x6b28d0 | 197 | `retire_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Please Confirm screen asking whether to resign from the club and nation jobs and retire from football. | high | opus |  |
| 0x6b2b40 | 161 | `retire_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the retire confirm buttons, removing the human manager from both jobs and clearing all player state on Yes. | high | opus |  |
| 0x6b2d60 | 8 | `open_holiday_screen` | cdecl, no arguments, returns void, ret 0 | Opens the Go on holiday confirm screen with its settings. | high | opus | 2026-10-15-holiday-next-match-inventory.md |
| 0x6b2d80 | 496 (+1 unwind) | `holiday_screen_build` | cdecl, no arguments, returns void, ret 0 | Builds the Go on holiday confirm screen with seven holiday setting checkboxes and No and Yes buttons. | high | opus | 2026-10-14-assistant-and-days-inventory.md, 2026-10-15-holiday-next-match-inventory.md, waits.c |
| 0x6b3440 | 212 | `holiday_screen_handle_action` | cdecl(short widget_index), returns int screen result, ret 0 | Handles the holiday screen widgets, recording the No or Yes answer and toggling the seven holiday settings. | high | opus | 2026-10-15-holiday-next-match-inventory.md |
| 0x6b36f0 | 397 | `compare_manager_stats_rows` | cdecl(staff_record *a, staff_record *b), returns int, ret 0 | Compares two manager stat records by the stat key and nation chosen on the Manager Stats screen, then by manager name. | high | opus |  |
| 0x6b3be0 | 14 | `compare_job_information_rows` | cdecl(job_row *a, job_row *b), returns int, ret 0 | Compares two Job Information rows by the signed 16 bit job security value at offset 8, putting null rows last. | high | opus |  |
