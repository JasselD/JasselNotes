**Controlling Access to Network Devices**
SSH & Telnet
- What?
	- Secure Shell (SSH) and Telnet are remote access protocols used to control network devices
- Why?
	- These protocols allow remote configuration and management of devices
- How?
	- SSH:
		- Secure, encrypted access to devices using a public/private key pair of devices
	- Telnet:
		- Older, unencrypted method used for remote access

**Switch Operations & MAC Table**
- What?
	- Switches operate by forwarding frames based on MAC (Media Access Control) addresses stored in the MAC address table
- Why?
	- This mapping allows switches to efficiently forward traffic only to the correct port
- How?
	- Forwarding Methods:
		- Store and Forward:
			- Stores entire frames and checks for errors before and forwarding
		- Cut-Through:
			- Forwards frames as soon as the destination MAC is recognized, without error checking

**VLANs (Virtual Local Area Networks)**
- What?
	- VLANs divide large physical networks into smaller, logical networks, improving security and traffic management
- Why?
	- To segragate traffic and improve network performance by reducing broadcast domains
- How?
	- Configuration on Switches:
		- Change VLAN name 
	- VLANs on Routers:
		- Routers route between different VLANs using Router-on-a-Stick configuration

**802.1Q Tagging & Native VLAN**
- What?
	- 802.1Q is a VLAN tagging protocol that allows multiple VLANs to travel over a single physical link
- Why?
	- To identify VLANs in a trunk link between switches
- How?
	- Native VLAN:
		- The VLAN that does not get tagged. Usually VLAN 1
	- Tagging Command

**Spanning Tree Protocol (STP)**
- What?
	- STP prevents network loops in a redundant network. setup by blocking redundant paths
- Why?
	- To avoid broadcast storms and ensure loop-free path
- How?
	- Root Bridge Election:
		- The lowe