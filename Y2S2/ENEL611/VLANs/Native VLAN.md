**Native VLAN**
- Native VLAN is used to carry untagged traffic across trunk links
- In 802.1Q trunking, a 4-byte VLAN tag is added to most frames
- Untagged frames e.g. from legacy devices, are placed into the Native VLAN
- Purpose:
	- Trunk ports allow multiple VLANs to share the same physical link
	- Untagged traffic on a trunk is assigned to the Native VLAN
	- On Cisco switches:
		- By default, the Native VLAN = VLAN 1
		- Best practice:
			- Change Native VLAN to an unused VLAN (not VLAN 1 or a Data VLAN)
			- Helps in enhancing security and preventing VLAN hopping attacks
- Example:
	- VLAN 99 is configured as the Native VLAN across all trunk ports
	- All regular user traffic is tagged, except some legacy traffic, which is associated with VLAN 99

[[Management VLAN]]
