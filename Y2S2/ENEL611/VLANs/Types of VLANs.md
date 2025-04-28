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

For example, **show vlan brief** "all ports are currently assigned to the default VLAN 1"
```
```Switch# **show vlan brief** VLAN Name Status Ports ---- ----------------- ------- -------------------- 1 default active Fa0/1, Fa0/2, Fa0/3, Fa0/4 Fa0/5, Fa0/6, Fa0/7, Fa0/8 Fa0/9, Fa0/10, Fa0/11, Fa0/12 Fa0/13, Fa0/14, Fa0/15, Fa0/16 Fa0/17, Fa0/18, Fa0/19, Fa0/20 Fa0/21, Fa0/22, Fa0/23, Fa0/24 Gi0/1, Gi0/2 1002 fddi-default act/unsup 1003 token-ring-default act/unsup 1004 fddinet-default act/unsup 1005 trnet-default act/unsup
