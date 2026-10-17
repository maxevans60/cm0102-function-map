# award_screens.cpp: 16 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x414a60 | 46 | `AWARD_MANAGER::find_award_by_staff_comp` | thiscall(AWARD_MANAGER* this, StaffComp* staff_comp) ret 4, returns AWARD* or 0 | Searches every award of the 30 nation award objects for the one whose staff competition matches and returns it. | high | opus |  |
| 0x414ac0 | 46 | `AWARD_MANAGER::find_award_by_club_comp` | thiscall(AWARD_MANAGER* this, ClubComp* comp) ret 4, returns AWARD* or 0 | Searches every award of the 30 nation award objects for the one linked to the given club competition and returns it. | high | opus |  |
| 0x414b20 | 12 | `award_rating_filter_reputation_over_2000` | cdecl(Staff* player, Fixture* fixture) ret 0, returns 1 or 0 | Accepts a player for the world year ratings when his current reputation exceeds 2000. | high | opus |  |
| 0x414b40 | 97 | `award_rating_filter_selected_nations` | cdecl(Staff* player, Fixture* fixture) ret 0, returns 1 or 0 | Accepts a player for the second year ratings when he or the fixture's competition belongs to Denmark, Belgium, France, Holland or Sweden. | high | opus |  |
| 0x414c20 | 58 | `award_screens_open_award_screen` | cdecl(StaffComp* staff_comp) ret 0 | Opens the award screen for the award of the given staff competition, or asserts when the argument is null. | high | opus |  |
| 0x414cf0 | 741 | `award_screen_draw` | cdecl(void) ret 0 | Draws the award screen with its competition, nationality or international title, award tabs, nominations button and the winners of the award. | high | opus |  |
| 0x415600 | 19 | `ScreenManager::add_menu_area` | thiscall(ScreenManager* this, int parent_item), ret 4, returns area id | Adds a display area with style 0x30 under the given parent item on the current screen's display. | medium | opus |  |
| 0x415640 | 31 | `ScreenManager::add_menu_item` | thiscall(ScreenManager* this, int area, const char* text, int link_type, void* link_data) ret 0x10 | Adds a text menu item with a link type and link data to a display area of the current screen of the screen manager. | medium | opus |  |
| 0x4156a0 | 749 | `award_screen_draw_year_award` | cdecl(int* top_y, int* bottom_y) ret 0 | Lists the past winners of a year award by season with the placed players and their clubs, or a no awards message. | high | opus |  |
| 0x415f60 | 807 (+1 unwind) | `award_screen_draw_team_award` | cdecl(int* top_y, int* bottom_y) ret 0 | Draws a team award page with the chosen eleven on a pitch diagram, its date and the previous and next year buttons. | high | opus |  |
| 0x416570 | 357 | `award_screen_draw_team_award_fragment_416570` | not a function entry: mid-instruction start inside award_screen_draw_team_award, no own ret | Forms part of the team eleven row loop of award_screen_draw_team_award and is a false function entry. | high | opus |  |
| 0x416960 | 270 | `award_screen_handle_action` | cdecl(int item_index) ret 0, returns screen action code | Handles a click on the award screen by opening another award, changing the view, opening nominations or paging the team award year. | high | opus |  |
| 0x416cb0 | 40 (+1 unwind) | `award_screens_open_nominations_from_news` | cdecl(int news_key_a, int news_key_b) ret 0 | Finds a news item and opens the nominations screen for the award of the award manager that its first two slots name. | high | opus |  |
| 0x416d50 | 69 | `award_screens_open_nominations_screen` | cdecl(AWARD* award) ret 0 | Opens the nominations screen for an award and records whether the human manager may still vote, or asserts on a null award. | high | opus |  |
| 0x416e40 | 389 | `award_nominations_screen_draw` | cdecl(void) ret 0 | Draws the nominations screen of an award with each shortlisted player, his club and nation, and Back and Next buttons. | high | opus |  |
| 0x4172f0 | 116 | `award_nominations_screen_handle_action` | cdecl(int item_index) ret 0, returns screen action code | Handles a click on the nominations screen by storing the chosen player as the human's vote and opening his profile, or clearing the vote. | high | opus |  |
