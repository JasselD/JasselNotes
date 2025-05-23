**VLAN Trunk**
- A trunk is a point-to-point link between two network devices (like switches) that can carry traffic for multiple VLANs
- Trunks allow VLAN traffic to travel between switches, so devices on different switches but in the same VLAN can communicate directly without needing a router
- Purpose:
	- Transport multiple VLANs over a single link
	- Does not belong to any specific VLAN, it acts as a conduit
	- Trunks are essential for VLANs to span across multiple switches
	- Default behaviour on Ciscop switches:
		- All VLANs are allowed on trunk links unless manually restricted
	- Trunks can also connect to servers with 802.1Q-capable network cards (NICs)
- Trunking Protocol
	- IEEE 802.1Q is the industry standard for trunking on:
		- Fast Ethernet
		- Gigabit Ethernet
		- 10-Gigabit Ethernet
	- 802.1Q Tagging:
		- Each Ethernet frame gets a 4-byte tag added to indicate which VLAN it belongs to
		- Frames from the native VLAN are not tagged
- Example:
	- Swtiches S1, S2, and S3 are connected using trunks
	- VLANs 10, 20, 30, and 99 (native VLAN) are allowed across the trunks
	- Devices in VLAN 10 on S1 can talk to devices in VLAN 10 on S2 through the trunk

![[Pasted image 20250428193201.png]]
