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
			- If the native VLAN is not reconfigured, the default PVID is 1
- Network Scenario: Flow of Untagged Traffic:
	- Network Setup:
		- Switches are interconnected with 802.1Q trunk links
		- A hub is used to connect PC1 to the network
		- The hub sends PC1's untagged traffic to the switches, which assign it to the native VLAN (VLAN 1)
	- Traffic Flow:
		- PC1 sends untagged traffic
		- Hub forwards it to switches
		- Switches forward the untagged traffic to the corerct ports, using the native VLAN configuration
		- Untagged frames are forwarded through the VLAN 1 port, but tagged frames on the trunk link are dropped by the switch
- Network Design Issues in Scenario:
	- Problems with this setup:
		- Using a hub is inefficient, as it broadcasts to all connected devices
		- PC1 is connected to a trunk link, which is unusual and poor design because trunks are meant to carry multiple VLAN traffic, not end-host traffic
		- Access ports are assigned to the native VLAN, which is generally discouraged
		- This topology illustrates legacy network designs that may require native VLAN handling to ensure compatibility