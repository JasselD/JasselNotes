Broadcast Domains
- A collection of interconnected switches
	- One large broadcast domain
- Only a network layer device (like a router) can split (divide) a Layer 2 broadcast domain
- Routers segment both broadcast domains and collision domains

Layer 2 Broadcast Details
- Layer 2 broadcast:
	- Frame's destination MAC address is set to all binary ones
		- Example: (FF:FF:FF:FF:FF:FF)
- Mac Broadcast Domain:
	- All devices to the LAN that receives and process Layer 2 broadcast frames

Switch Behavior with Broadcasts
- When a switch receives a broadcast frame:
	- It forwards the frame out of every port, except the one it came in on (ingress port)
	- Every device connected to the switch receives a copy of the broadcast frame

Impact of Broadcast
- Broadcast are sometimes necessary:
	- For example, for locating devices or servies (like ARP)
	- 