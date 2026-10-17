# tcpip.cpp: 18 functions

Function map of cm0102.exe 3.9.68. Generated from the Bosman Edition repo. Do not edit by hand: report a wrong name as an issue.

AI agents named each function from its code, and a review checked every medium and low name. Treat a medium or low name as a hint and read the code before you rely on it. "Cited in" lists research docs of the Bosman Edition repo that name the address.

| Address | Size | Name | Convention | Purpose | Confidence | Model | Cited in |
|---|---|---|---|---|---|---|---|
| 0x8ae0d0 | 31 | `parse_ipv4_address` | stdcall(sockaddr_in *out, const char *dotted_address) ret 8 | Fills an IPv4 socket address from a dotted quad string, with family AF_INET and port zero. | high | opus |  |
| 0x8ae140 | 19 | `format_ipv4_address` | stdcall(const sockaddr_in *address, char *out) ret 8 | Writes the four address bytes of an IPv4 socket address into a buffer as a dotted quad string. | high | opus |  |
| 0x8ae180 | 59 | `TcpIp::TcpIp` | thiscall(TcpIp* this, short max_connections), returns this, ret 4 | Builds the TCP/IP object, sets every connection, listen and broadcast socket to invalid and allocates the connection socket table. | high | opus |  |
| 0x8ae260 | 22 | `TcpIp::start_winsock` | thiscall(TcpIp* this), returns bool, ret 0 | Starts Winsock 1.1 once, then runs the loopback connection test and reports whether TCP/IP works. | high | opus |  |
| 0x8ae2a0 | 53 | `TcpIp::close_all_sockets` | thiscall(TcpIp* this), ret 0 | Closes every connection, listen and broadcast socket, marks each invalid and shuts Winsock down when it was started. | high | opus |  |
| 0x8ae340 | 18 | `TcpIp::close_connection` | thiscall(TcpIp* this, short slot), ret 4 | Closes the socket in one connection slot and marks that slot invalid. | high | opus |  |
| 0x8ae370 | 198 | `TcpIp::open_listen_sockets` | thiscall(TcpIp* this, ushort port), returns int any_open, ret 4 | Opens a non-blocking TCP listen socket on each local adapter address at the given port, and returns true when at least one opens. | high | opus |  |
| 0x8ae640 | 166 | `TcpIp::connect_to_host` | thiscall(TcpIp* this, ushort port, address* host), returns short slot, ret 8 | Connects a new non-blocking TCP socket in a free connection slot to the host address and port, and returns the slot or -1. | high | opus |  |
| 0x8ae840 | 61 | `TcpIp::accept_connection` | thiscall(TcpIp* this), returns short slot, ret 0 | Accepts a waiting connection on any listen socket and stores it in a free connection slot, or closes it when the table is full. | high | opus |  |
| 0x8ae8d0 | 98 | `TcpIp::send_to_connection` | thiscall(TcpIp* this, short slot, const void* data, int length), returns int sent, ret 0xc | Sends data on one connection socket, retries while the socket would block, and closes the slot on any other error. | high | opus |  |
| 0x8ae9c0 | 69 | `TcpIp::receive_from_connection` | thiscall(TcpIp* this, short slot, void* buffer, int length), returns int received, ret 0xc | Receives data from one connection socket, returns zero when no data waits and closes the slot on an error or a disconnect. | high | opus |  |
| 0x8aea80 | 137 | `TcpIp::open_broadcast_sockets` | thiscall(TcpIp* this, ushort port), returns int any_open, ret 4 | Opens a non-blocking UDP broadcast socket on each local adapter address at the given port, and returns true when at least one binds. | high | opus |  |
| 0x8aec60 | 16 | `TcpIp::close_broadcast_sockets` | thiscall(TcpIp* this), ret 0 | Closes the twenty UDP broadcast sockets and marks each invalid. | high | opus |  |
| 0x8aec90 | 76 | `TcpIp::send_datagram` | thiscall(TcpIp* this, const void* data, int length, ushort port, sockaddr* to, int to_length, short socket_index), returns int sent, ret 0x18 | Sends a datagram to the broadcast address of every adapter when no address is given, or to one address through one broadcast socket. | high | opus |  |
| 0x8aed80 | 52 | `TcpIp::receive_datagram` | thiscall(TcpIp* this, void* buffer, int length, sockaddr* from, int* from_length, short* socket_index_out), returns int received, ret 0x14 | Reads the first waiting datagram from the twenty broadcast sockets and reports the sender and the socket index. | high | opus |  |
| 0x8aee00 | 10 | `TcpIp::can_resolve_address` | thiscall(TcpIp* this unused, sockaddr_in* address), returns bool, ret 4 | Reports whether the host at the address of a sockaddr resolves through a reverse name look-up. | high | opus |  |
| 0x8aee20 | 348 | `tcpip_scan_adapter_addresses` | stdcall(adapter_entry* table, short* count_out), ret 8 | Runs winipcfg, ip.exe or ipconfig into a file, parses each adapter address and subnet mask and computes its broadcast address. | high | opus |  |
| 0x8af290 | 216 | `TcpIp::test_loopback_connection` | thiscall(TcpIp* this), returns int works, ret 0 | Tests TCP/IP by opening a listen socket on 127.0.0.1 port 6667 and connecting a second socket to it, then closes both. | high | opus |  |
