What is a VLAN?
VLAN (Virtual LAN):
- Creates logical groupings of devices, not based on physical connections
- Devices within a VLAN communicate anywhere (different switches, different floors) and still be part fo the same VLAN
- Flexibility:
	- Devices can be anywhere (different switches, different floors) and still be part of the same VLAN

Example Setup
- 3-Floor Building with switches on each floor
- VLANs span all three floors:
	- VLAN 2 (IT) -> Network: 10.0.2.0/24
	- VLAN 3 (HR) -> Network: 10.0.3.0/24
	- VLAN 4 (Sales) -> Network: 10.0.4.0/24
- All VLANs connect through an additional switch linked to a router

Key Points
- Logical Networks:
	- Each VLAN acts as a separate independent network
- Switch Ports:
	- Any switch port can be assigned to only one VLAN (except trunk ports or IP phone ports)
- Packet Forwarding:
	- Unicast, Broadcast, and Multicast packets stay within their VLAN
	- To send packets between VLANs, routing is needed (eg. a router or a Layer 3 switch)

Benefits:
- Smaller Broadcast Domains:
	- Reduces unnecessary broadcast traffic -> better network performance
- Segmentation by Functions:
	- Segmetn based on department, team, application, etc., not physical location
- Security and Access Control:
	- Different policies can be applied to different VLANs

Without VLANs (Flat Network)
- Even with multiple IP subnets:
	- All devices would still be in the same Layer 2 broadcast domain
	- Broad