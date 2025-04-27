Step 1: Learn (Examing the Source MAC Address)
- Every frame that enters the switch is inspected
- Source MAC not in the table:
	- Add MAC address and incoming port to the MAC address table
- Source MAC already in the table:
	- Same port: Just refresh the timer (default: 5 minutes)
	- Different port: Update the entry with the new port number

Step 2: Forward (Examining the destination MAC Address)
- Destination MAC is unicast address:
	- Found in table: Forward frame out the matched port
	- Not found in table: Flood frame out all ports (except incoming ports) Unknown unicast
- Destination MAC is broadcast or mulitcast;:
	- Always flood the frame out all ports (except the incoming port)

[[Unicast and Multicast]]
