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
[[Controlling Access to Network Devices]]

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
[[Switch Operations & MAC Table]]

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
[[VLANs]]

**802.1Q Tagging & Native VLAN**
- What?
	- 802.1Q is a VLAN tagging protocol that allows multiple VLANs to travel over a single physical link
- Why?
	- To identify VLANs in a trunk link between switches
- How?
	- Native VLAN:
		- The VLAN that does not get tagged. Usually VLAN 1
	- Tagging Command
[[802.1Q Tagging & Native VLAN]]

**Spanning Tree Protocol (STP)**
- What?
	- STP prevents network loops in a redundant network. setup by blocking redundant paths
- Why?
	- To avoid broadcast storms and ensure loop-free path
- How?
	- Root Bridge Election:
		- The lowest Bridge ID (MAC + priority) becomes the Root Bridge
	- Port Roles:
		- Root Port: The port closest to the root bridge
		- Designated Port: The poer that sends traffic for the network segment
		- Alternate Port: Blocked port that can be used if the root port fails
[[Spanning Tree Protocol (STP)]]

**Securing Switches Against Attacks**
MAC Address Attacks
- What?
	- Attackers flood the MAC table with fake addresses, causing the switch to fail and broadcast traffic to all ports
- How to Prevent?
	- Port security
	- Action:
		- Shutdown or restrict mode on violation
- DHCP Spoofing
	- What?
		- Attackers send fake DHCP offers to clients, causing them to connect to malicious servers
	- How to Prevent?
		- DHCP Snooping
- VLAN Hopping & Double Tagging Attacks
	- What?
		- Attackers manipulate VLAN tags to send frames to unauthorized VLANs
	- How to Prevent?
		- Disable unused VLANs and restrict access to trunk ports
- ARP Attacks
	- What?
		- Attackers send false ARP messages, causing devices to send data to the attacker
	- How to Prevent?
		- Dynamic ARP Inspection (DAI)
[[DHCP Attacks and Mitigation]]

**EtherChannel**
- What?
	- EtherChannel is a link aggregation technology that combines multiple physical links into a single logical link to increase bandwidth
- Why?
	- To improve performance and provide redundancy
- How?
	- Configuration Command
[[EtherChannel]]

**IPv4 & IPv6 Address Provisioning**
- IPv4 Addressing
	- What?
		- IPv4 assigns 32-bit addresses to devices on a network
	- How to Assign?
		- Static IP Configuration or via DHCP
- IPv6 Addressing
	- What?
		- IPv6 assigns 128-bit addresses, solving the IPv4 address shortage
	- How?
		- Stateless SLAAC (Stateless Address Autoconfiguration):
			- Devices automatically generate their IPv6 address based on Router Advertisements
		- Stateful DHCPv6
[[IPv4 Address Provisioning]]
[[IPv6 Address Provisioning]]

**Wireless LAN & Security**
- Access Points (APs)
	- What?
		- Autonomous APs operate independently, while Controller-based APs are managed by a central controller
	- Why?
		- Controller-based APs simplify management in larger networks
	- How?
		- Autonomous AP configuration
		- Controlelr-based AP:
			- Uses centralized configuration and management
- Securing WLAN
	- What?
		- Secure wireless networks using WPA and WPA2 protocols
	- Why?
		- To prevent unauthorized access and eavesdropping
	- How?
		- Authentication Methods:
			- Personal (PSK): Pre-shared keys
			- Enterprise (EAP): Uses a RADIUS server for authentication
		- Encrpytion:
			- WEP (weak, outdated)
			- WPA/WPA2 (Stronger security)
[[Wireless LAN - Autonomous Access Points, Controller-based APs]]
[[Securing WLAN]]

**Routing: Static & Dynamic**
- Static Routing
	- What?
		- Manually configured devices
	- Why?
		- For small networks or where predictability is required
	- How?
		- Command
- Default Routes & Next Hop
	- What?
		- Default routes provides a last resort path for packets
	- How?
		- Command
- Floating Routes
	- What?
		- Backup routes with a higher administrative distance that only become active if the primary route fails
[[Routing - Static Routing, Routing Table, Default Routes, Next Hop, Local Routes, Floating Routes]]