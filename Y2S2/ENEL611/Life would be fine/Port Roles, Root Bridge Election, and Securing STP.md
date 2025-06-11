# Port Roles in STP
- STP assigns different roles to the switch ports depending on their position in the network topology. These roles determine whether the port will be used for forwarding traffic, blocking traffic, or acting as a backup
	- Root Port (RP):
		- What?
			- The port on a non-root bridge that is closest to the Root Bridge. It is the port that receives the best path to the Root Bridge
		- Why?
			- The Root Port ensures that the switch has a path to the Root Bridge for forwarding traffic
		- Example:
			- If a switch has multiple paths to the Root Bridge, the Root Port is the one with the lowest cost (best path)
			
	- Designated Port (DP):
		- What?
			- The port on a switch that forwards traffic for a given network segment (VLAN). It is the forwarding port on each segment
		- Why?
			- The Designated Port is responsible for sending data towards other switches and devices on that segment
		- Example:
			- For each network segment (ie., a cable or switch port), there is only one Designated Port to avoid conflicts
			
	- Blocked/Alternate Port:
		- What?
			- Ports that are not forwarding traffic to prevent network loops. These are backup paths will be used if the Root Port fails
			
		- Why?
			- To prevent redundant paths from causing loops in the network

## Root Bridge Election Process
- Root Bridge is the central switch in the STP topology. It serves as the reference points for all other switches. The Root Bridge Election process happens as follows:
	- Initial Election:
		- When STP starts, every switch assumes it is the Root Bridge and sends a BDPU (Bridge Protocol Data Unit) with its Bridge ID
		- The Bridge ID consists of the priority value and MAC address of the switch
		- Default priority is 32768, and the MAC address is unique to each switch
		
	- Choosing the Root Bridge:
		- The switch with the lowest Bridge ID (priority + MAC address) is elected as the Root Bridge
		- The Root Bridge does not have a Root Port (because it si the topmost bridge), but all other switches' Root Ports will point to the Root Bridge
		
	- Re-election:
		- If the Root Bridge fails, the election process is repeated, and a new Root Bridge is selected based on the lowest Bridge ID

## How Port Roles Are Determined
- Root Port (RP):
	- The port on the non--root switch that provides the best (lowest-cost) path to the Root Bridge
	
- Designated Port (DP):
	- The port on each network segment that is selected to forward traffic for that segment
	
- Alternate Port:
	- Ports that block traffic to avoid loops but will be used if the Root Port fails

# Securing STP to Prevent Attacks
- Although STP is designed to prevent loops, it is vulnerable to certain attacks that can compromise network stability and security. How to secure STP:
	- BDPU Guard:
		- What?
			- BDPU Guard disables ports that receive BDPUs (Bridge Protocol Data Units) from an unauthorized device, preventing rogue devices from becoming part of the STP