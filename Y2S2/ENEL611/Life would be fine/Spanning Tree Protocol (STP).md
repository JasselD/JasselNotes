# STP
- What?
	- Layer 2 protocol used to <mark style="background: #ABF7F7A6;">prevent loops in a network with redundant paths</mark>
	- Loops occur when <mark style="background: #ABF7F7A6;">multiple network path exist between switches</mark>, and without STP, frames could <mark style="background: #ABF7F7A6;">circulate endlessly</mark>, causing a <mark style="background: #ABF7F7A6;">broadcast storm</mark> and <mark style="background: #ABF7F7A6;">network congestion</mark>
	- STP ensures there is only <mark style="background: #ABF7F7A6;">one active path</mark> between any two devices in a network, <mark style="background: #ABF7F7A6;">blocking the redundant paths to avoid loops</mark>
- Why?
	- Loop Prevention:
		- Without STP, switches would <mark style="background: #ABF7F7A6;">broadcast traffic to all ports</mark>. When loops exist, the traffic gets <mark style="background: #ABF7F7A6;">duplicated</mark>, causing the network to become <mark style="background: #ABF7F7A6;">unresponsive</mark>
		
	- Redundancy:
		- STP allows <mark style="background: #ABF7F7A6;">network redundancy</mark>. If one link fails, STP automatically activates a <mark style="background: #ABF7F7A6;">backup path</mark>, keeping the network stable and available
		
- How?
	- Root Bridge Election:
		- <mark style="background: #ABF7F7A6;">STP elects a Root Bridge</mark>, which is the <mark style="background: #ABF7F7A6;">central reference point for the network</mark>. This bridge is chosen based on the <mark style="background: #ABF7F7A6;">lowest Bridge ID (priority + MAC address)</mark>
		- Why? The Root Bridge serves as the <mark style="background: #ABF7F7A6;">logical center of the network</mark>, and all switches calculate the <mark style="background: #ABF7F7A6;">best path</mark> to it
		
	- Port Roles:
		- Once the Root Bridge is elected, each switch determines the role of each port relative to the Root Bridge. This port roles include:
			- <mark style="background: #ABF7F7A6;">Root Port (RP)</mark>:
				- The port on a switch that has the shortest path to the Root Bridge
				
			- <mark style="background: #ABF7F7A6;">Designated Port (DP)</mark>:
				- The port on a switch that sends traffic towards the network segment. It is the forwarding port
				
			- Blocked/Alternative Port:
				- Ports that are not forwarding traffic to prevent loops
				
	- STP States:
		- Blocking:
			- The port does not forward frames and is not part of the forwarding path
			
		- Listening:
			- The switch listens to BDPUs (Bridge Protocol Data Units) to learn network topology changes
			
		- Learning:
			- The switch builds its MAC table but does not forward frames yet
			
		- Forwarding:
			- The port forwards traffic and is part of the active forwarding path
			
	- BPDUs (Bridge Protocol Data Units):
		- BDPUs are special frames exchanged between switches to share topology information. They help in the Root Bridge election and are used to maintain the network's spanning tree structure

# Root Bridge Election Process
- Each switch sends out a BDPU with its Bridge ID (priority + MAC address). The switch with the lowest Bridge ID becomes the Root Bridge
	- Example BDPU Format:
		- Priority (default: 32768)
		- MAC address (unique to each switch)

# Port Roles and How They Are Chosen
- Root Port (RP):
	- The port closest to the Root Bridge. Each switch has only one Root Port
	
- Designated Port (DP):
	- The port that forwards traffic for a particular network segment. Every segment has one Designated Port
	
- Alternate Port:
	- The port that is blocked to prevent network loops. It is used in case the Root Port fails

# Spanning Tree Algorithm
- STP uses the Spanning Tree Algorithm (STA) to determine the best path to the Root Bridge
- STP states are used to ensure only one active path between switches and block redundant paths

# Common STP Terms
- BPDU (Bridge Protocol Data Units):
	- The frames used by STP to share topology information
- Root Bridge:
	- The switch with the lowest Bridge ID
- Root Port (RP):
	- The port on a non-root bridge closest to the Root Bridge
- Designated Port (DP):
	- The port on switch that forwards traffic for a specific segment
- Alternate Port:
	- The port that is blocked to prevent loops
- Loop Prevention:
	- Ensures there's only one active path between any two devices

## QNA
- What is the main purpose of Spanning Tree Protocol (STP)
	- The main purpose of STP is to **prevent network loops** in a redundant network topology and to ensure **only one active path** is used between switches, keeping the network **stable**.
	
- What is the Root Bridge, and how is it elected in STP?
	- The **Root Bridge** is the central reference point for the network. It is elected based on the **lowest Bridge ID** (which includes a **priority** and **MAC address**). The switch with the **lowest** Bridge ID becomes the Root Bridge.
	
- What are the three main port roles in STP?
	- **Root Port (RP)**: The port closest to the Root Bridge.
    
	- **Designated Port (DP)**: The port that forwards traffic for a network segment.
    
	- **Alternate Port**: The port that is **blocked** to prevent loops but can be used if the Root Port fails.
	
- What is the difference between Root Port (RP) and Designated Port (DP)?
	- The **Root Port** is the port on a non-root bridge that provides the **shortest path** to the Root Bridge, whereas the **Designated Port** is the port that **forwards traffic** towards a particular network segment.
	
- What does the BDPU contain, and what is its role in STP?
	-  **BPDUs (Bridge Protocol Data Units)** contain information such as the **Bridge ID**, **Root Bridge ID**, and **path cost** to the Root Bridge. They are used by switches to share **topology information** and to elect the **Root Bridge**.