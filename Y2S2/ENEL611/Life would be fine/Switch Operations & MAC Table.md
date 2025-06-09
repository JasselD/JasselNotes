**Switch**
- What?
	- <mark style="background: #ABF7F7A6;">Layer 2 device</mark> in the OSL model that operates at the <mark style="background: #ABF7F7A6;">Data Link Layer</mark>
	- Function is to <mark style="background: #ABF7F7A6;">forward frames</mark> (data packets at Layer 2) based on <mark style="background: #ABF7F7A6;">MAC</mark> (Media Access Control) addresses
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
		- When a frame is received, the switch checks if the destination MAC address it already in the table. 
		- If found, it forwards the frame to the corresponding port
		- If not found, it broadcast the frame to all ports except the one it came from
- What happens if a MAC Address if not in the table?
	- If the destination MAC address is not in the MAC table, the switch will broadcast the frame to all ports except the port it was received form (flood)
	- The is normal behaviour in a netwrok until the switch learns the destination MAC address and adds it to the MAC table for future reference

**Forwading Methods**
- Switches can use different methods to forward frames
	- Store-and-Forward:
		- Stores the entire frame and checks it for errors (CRC errors) before forwarding it to the appropriate port
		- Pros: Error-free transmission
		- Cons: Slightly slower because waits for the entire frame
	- Cut-through:
		- Begins forwarding the frame as soon as it knows the destination MAC address, without error-checking
		- Pros: Faster forwarding
		- Cons: Risk of forwarding corrupted frames

**<mark style="background: #ABF7F7A6;">QNA</mark>
- What is the primary function of a switch
	- A switch **forwards frames** based on the **MAC address**. It efficiently delivers data to the correct port on the network.
	
- What does a switch do if it does not know the destination MAC address?
	- The switch will **broadcast** the frame to all ports, except the one it came from, until it learns the MAC address.
	
- What is the difference between store-and-forawrd and cut-through forwarding methods?
	- **Store-and-Forward**: The switch waits to receive the entire frame and checks for errors before forwarding. It's slower but more reliable.
    
	- **Cut-through**: The switch starts forwarding the frame as soon as it knows the destination MAC address, without checking for errors. It's faster but may forward corrupted frames.
	
- How does a switch learn MAC addressess?
	- The switch learns MAC addresses by inspecting the **source MAC address** of incoming frames and associating them with the **port** they arrived on.
	
- What does the 'show mac address-table' command display?
	- The **MAC address table** shows the **MAC addresses** associated with each **port** on the switch, along with their **VLAN** and the type of entry (dynamic or static).