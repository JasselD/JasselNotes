**Switch**
- What?
	- Layer 2 device in the OSL model that operates at the Data Link Layer
	- Function is to forward frames (data packets at Layer 2) based on MAC (Media Access Control) addresses
	- Fundamental in local area networks (LANs), as they ensure efficient data delivery by sending traffic only to the specific port that needs it
- How?
	- Learns the MAC addressess of devices that are connected to each of its port
	- It then stores these addressess in a MAC address table (forwarding table)
	- When frames is received, the switch checks its MAC address table to see if it has an entry for the destination MAC address. If found, it forwards the frame to the correct port

**MAC Address Table**
- What?
	- Database that maps MAC addresses to specific ports on the switch
	- Learning Process:
		- When a switch receives a frame, it reads the source MAC address and the port it arrived on, then adds this information to its MAC table
	- Forwarding Process:
		- When a frame is received, the switch checks if the destination MAC address it already in t