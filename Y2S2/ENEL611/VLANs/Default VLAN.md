**Default VLAN**
- VLAN 1 is the default VLAN on all Cisco switches
- All switches ports are intially part of VLAN 1
- Default VLAN is used for control traffic like CDP (Cisco Discovery Protocol), STP (Spanning Tree Protocol), etc (Layer 2 control traffic)
- Even after creating new VLANs, VLAN 1 cannot be deleted or renamed
- Important Facts about VLAN 1
	- All ports are assigned to VLAN 1 initially
	- The Native VLAN is VLAN 1 by default
	- The Management VLAN is VLAN 1 by default
	- VLAN 1 cannot be renamed or deleted
	- Security Risk:
		- Having Native VLAN = Management VLAN (both VLAN 1) is considered a security vulnerability
		- Best practice: Change the management VLAN and use a differrent native VLAN
- For example, **show vlan brief** "all ports are currently assigned to the default VLAN 1"
	- ![[Pasted image 20250428174248.png]]


[[Data VLAN]]
