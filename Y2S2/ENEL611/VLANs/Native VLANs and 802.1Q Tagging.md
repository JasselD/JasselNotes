**IEEE 802.1Q**
- 802.1Q specifies a native VLAN for trunk links
- By default, VLAN 1 is the native VLAN for trunk links
- When untagged frames arrive at a trunk port, they are assigned to the native VLAN

**Tagging vs Untagged Frames on Native VLAN**
- Tagged Frames on the Native VLAN
	- Normally, native VLAN traffic should not be tagged
	- If an 802.1Q trunk port receives a tagged frame with the same VLAN ID as the native VLAN, it drops the frame
	- Devices that add tags to native VLAN traffic include IP phones, routers, and non-Cisco switches
	- Cisco best practice: Configure devices to not send tagged frames on the native VLAN
- Untagged Frames on the Native VLAN
	- If a Cisco switch trunk port receives untagged frames (whcih are uncommon), the switch assigns them to the native VLAN
	- If there are no devices in the native VLAN or no other trunk ports, the untagged frames may be dropped
	- The default native VLAN is VLAN 1
	- The PVID (Port VLAN ID) is used to forward untagged traffic.
		- For example:
			- If VLAN 99 is set as the native VLAN, the PVID is 99
			- If the native VLAN is not reconfigured, the dedau