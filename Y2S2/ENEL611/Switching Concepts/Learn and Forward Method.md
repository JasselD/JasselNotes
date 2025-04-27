Step 1: Learn (Examing the Source MAC Address)
- Every frame that enters the switch is inspected
- Source MAC not in the table:
	- Add MAC address and incoming port to the MAC address table
- Source MAC already in the table:
	- Same port: Just refresh the timer (default: 5 minutes)
	- Different port: Update the entry with the new port number

Step 2: 