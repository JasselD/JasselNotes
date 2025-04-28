**Management VLAN**
- Management VLAN is a special VLAN used only for network management traffic
- It handles important administrative connections like:
	- SSH
	- Telnet
	- HTTPS/HTTP (for web-based management)
	- SNMP (Simple Network Management Protocol)
- Purpose:
	- To seperate management traffic from user/data traffic for security and organisations
	- Default settings:
		- VLAN 1 is the default Management VLAN on Cisco switches
	- Best Pratice:
		- Create a dedicated, separate VLAN for management (not VLAN 1) to enchance security
	- Only network administrator should have access to devices on the Management VLAN
- Example:
	- VLAN 99 = Management VLAN
	- Network admins connect to switches IP addresses inside VLAN 99 via SSH to configure and monitor devices

[[Voice VLAN]]
