**How Broadcast Work in a Non-VLAN Network**
- No VLANs = One broadcast domain covering the entire network
- When a switch receives a broadcast frame on a port, it forwards the frame to all other ports, except the one it was received on
- Scenario (Single Subnet Network):
	- Imagine a network where everything is in the same subnet, 172.17.40.0/24
	- No VLANs configured = everything is in the same broadcast domain
- Example:
	- PC1 (Faculty computer) sends a broadcast frame
	- 