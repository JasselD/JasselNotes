# TCP Three-Way Handshake
- What?
	- Process used to establish a reliable connection between a client and server in a TCP/IP network. This handshake ensures synchronization between sender and receiver before actual data is transmitted

# Steps (SYN-SYN/ACK-ACK)
- SYN
	- The clients initiates the connection with a SYN (synchronize) message
	- Who sends it?:
		- Client
	- Purpose:
		- "Hey, I want to start a connection"
- SYN-ACK
	- The server replies with SYN-ACK (synchronize + acknowledgement)
	- Who sends it?:
		- Server
	- Purpose:
		- "Okay,"