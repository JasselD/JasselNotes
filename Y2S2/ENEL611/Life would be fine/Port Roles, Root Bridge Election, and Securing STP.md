# Port Roles in STP
- STP assigns <mark style="background: #ABF7F7A6;">different roles to the switch ports</mark> depending on <mark style="background: #ABF7F7A6;">their position in the network topology</mark>. These roles determine whether the port will be used for <mark style="background: #ABF7F7A6;">forwarding traffic, blocking traffic, or acting as a backup</mark>
	- Root Port (RP):
		- What?
			- The port on a non-root bridge that is <mark style="background: #ABF7F7A6;">closest to the Root Bridge</mark>. It is the port that <mark style="background: #ABF7F7A6;">receives the best path</mark> to the Root Bridge
		- Why?
			- The Root Port ensures that the <mark style="background: #ABF7F7A6;">switch has a path to the Root Bridge</mark> for f<mark style="background: #ABF7F7A6;">orwarding traffic</mark>
		- Example:
			- If a switch has <mark style="background: #ABF7F7A6;">multiple paths</mark> to the Root Bridge, the Root Port is the one with the <mark style="background: #ABF7F7A6;">lowest cost (best path)</mark>
			
	- Designated Port (DP):
		- What?
			- The port on a switch that <mark style="background: #ABF7F7A6;">forwards traffic for a given network segment (VLAN)</mark>. It is the <mark style="background: #ABF7F7A6;">forwarding port on each segment</mark>
		- Why?
			- The Designated Port is responsible for <mark style="background: #ABF7F7A6;">sending data towards other switches and devices on that segment</mark>
		- Example:
			- For each network segment (ie., a cable or switch port), there is <mark style="background: #ABF7F7A6;">only one Designated Port to avoid conflicts</mark>
			
	- Blocked/Alternate Port:
		- What?
			- Ports that are <mark style="background: #ABF7F7A6;">not forwarding traffic</mark> to <mark style="background: #ABF7F7A6;">prevent network loops</mark>. These are <mark style="background: #ABF7F7A6;">backup paths</mark> will be used if the <mark style="background: #ABF7F7A6;">Root Port fails</mark>
			
		- Why?
			- To prevent redundant paths from causing loops in the network

## Root Bridge Election Process
- Root Bridge is the central switch in the STP topology. It serves as the reference points for all other switches. The Root Bridge Election process happens as follows:
	- Initial Election:
		- When STP starts, every switch <mark style="background: #ABF7F7A6;">assumes</mark> it is the Root Bridge and sends a <mark style="background: #ABF7F7A6;">BDPU (Bridge Protocol Data Unit) with its Bridge ID</mark>
		- The Bridge ID consists of the <mark style="background: #ABF7F7A6;">priority value</mark> and <mark style="background: #ABF7F7A6;">MAC address</mark> of the switch
		- Default priority is <mark style="background: #ABF7F7A6;">32768</mark>, and the MAC address is unique to each switch
		
	- Choosing the Root Bridge:
		- The switch with the <mark style="background: #ABF7F7A6;">lowest Bridge ID (priority + MAC address)</mark> is elected as the Root Bridge
		- The Root Bridge <mark style="background: #ABF7F7A6;">does not have a Root Port</mark> (because it is the <mark style="background: #ABF7F7A6;">topmost bridge</mark>), but all other switches' Root Ports will point to the Root Bridge
		
	- Re-election:
		- If the Root Bridge fails, the <mark style="background: #ABF7F7A6;">election process is repeated</mark>, and a new Root Bridge is selected based on the <mark style="background: #ABF7F7A6;">lowest Bridge ID</mark>

## How Port Roles Are Determined
- Root Port (RP):
	- The port on the non--root switch that provides the <mark style="background: #ABF7F7A6;">best (lowest-cost) path</mark> to the Root Bridge
	
- Designated Port (DP):
	- The port on each network segment that is selected to forward traffic for that segment
	
- Alternate Port:
	- Ports that block traffic to avoid loops but will be used if the Root Port fails

# Securing STP to Prevent Attacks
- Although STP is designed to prevent loops, it is vulnerable to certain attacks that can compromise network stability and security. How to secure STP:
	- BDPU Guard:
		- What?
			- BDPU Guard disables ports that receive BDPUs (Bridge Protocol Data Units) from an unauthorized device, preventing rogue devices from becoming part of the STP topology
			
		- How?
			- When BPDU Guard is enabled, if a BDPU is received on a port in PortFast mode, the port is shut down immediately
			
	- Root Guard:
		- What?
			- Root Guard prevents a switch from becoming the Root Bridge by blocking any BDPUs with a lower priority or higher MAC address than the current Root Bridge
			
		- How?
			- This prevents rogue switches from becoming the Root Bridge and disrupting the STP topology
			
	- Loop Guard:
		- What?
			- Loop Guard prevents a blocked port from becoming unblocked unexpectedly. This protects againts forwarding loops of the network topology changes unexpectedly
			
		- How?
			- If the STP state of a port changes unexpectedly (e.g, from blocked to forwarding), Loop Guard will keep it in a blocked state
			
	- PortFast:
		- What?
			- The PortFast feature allows ports to immediately transition to the forwarding state, bypassing the usual STP listening and learning states
			
		- Why?
			- This is useful for end-devices like computers or printers that don't participate in STP
			
		- How?
			- PortFast should only be used on access ports (ports that connect to end-user devices)

## QNA
- What is the role of the Root Port (RP) in STP?
	- The **Root Port (RP)** is the port on a non-root bridge that provides the **shortest path** to the Root Bridge. It’s the **best port** for forwarding traffic towards the Root Bridge.
	
- How is the Root Bridge elected in STP?
	- The **Root Bridge** is elected based on the **lowest Bridge ID**, which includes the **priority** (default is 32768) and the **MAC address**. The switch with the lowest **Bridge ID** becomes the Root Bridge.
	
- What are the three main port roles in STP?
	-  **Root Port (RP)**: The port closest to the Root Bridge.
        
    - **Designated Port (DP)**: The port that forwards traffic for a specific network segment.
        
    - **Alternate Port**: The port that is **blocked** to prevent loops but can be used if the Root Port fails.
    
- What is BDPU Guard, and how does it secure STP?
	- **BPDU Guard** disables ports that receive BPDUs from unauthorized devices, preventing rogue switches from interfering with the STP topology.
	
- What is the difference between Root Guard and Loop Guard?
	- **Root Guard** prevents unauthorized switches from becoming the Root Bridge by blocking BPDUs from them.
    
	- **Loop Guard** ensures that a port stays **blocked** if it unexpectedly transitions out of a blocking state, preventing potential forwarding loops.