# plot.cpp: 6 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x7c6fc0 | 58 | `Plot::Plot` | thiscall(Plot* this, int min_x, int min_y, int max_x, int max_y, int max_series) ret 0x14 | Stores the value range of a line graph and allocates an array of 0x12 byte series slots, showing an error box when the allocation fails. | high | opus |  |
| 0x7c70a0 | 38 | `Plot::~Plot` | thiscall(Plot* this) ret 0 | Frees the point array and label string of every series slot, then frees the series array of the graph. | high | opus |  |
| 0x7c7100 | 94 | `Plot::add_series` | thiscall(Plot* this, int max_points, short colour, const char* label) ret 0xc | Appends a series with room for a number of points, a colour and a copied label to the graph, or shows an error when full. | high | opus |  |
| 0x7c7240 | 74 | `Plot::add_point` | thiscall(Plot* this, int series, int x, int y) ret 0xc | Appends one x and y point to a series of the graph, or shows an error when the series or point index is too high. | high | opus |  |
| 0x7c7340 | 209 | `Plot::draw_line_graph` | thiscall(Plot* this, int x0, int y0, int x1, int y1, char* x_title, char* y_title) ret 0x18 | Draws the axes of a line graph, then scales each series of points into the plot area and draws them as coloured line segments. | medium | opus |  |
| 0x7c7580 | 794 | `Plot::draw_axes` | thiscall(Plot* this, int x0, int y0, int x1, int y1, int pad_range, char* x_title, char* y_title) ret 0x1c | Draws the graph area, both axis lines, the axis titles and the numbered tick labels, widening the value range by one when asked. | medium | opus |  |
