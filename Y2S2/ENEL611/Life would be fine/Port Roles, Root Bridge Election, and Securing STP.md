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

# Root Bridge Election Process
- Root Bridge is the central switch in the STP topology. It serves as the reference points for all other switches. The Root Bridge Election process happens as follows:
	- Initial Electi