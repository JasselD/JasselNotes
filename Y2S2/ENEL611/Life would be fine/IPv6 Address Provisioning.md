# IPv6 Address Provisioning
- What?
	- Next generation of the IP protocol, offering 128-bit addresses, which vastly increase the number of available IP addresses compared to IPv4 (32-bits)
	- Refers to process of assigning IPv6 addresses to devices, either statically or dynamically

## IPv6 Address Types
- Global Unicast Address (GUA):
	- GUAs are globally routable on the internet
	
	- Example:
		- 2001:0db8:85a3:0000:0000:8a2e:0370:7334
		
- Link-Local Addres:
	- Link-local addresses are only valid within a single network segment (i.e, not routable beyond the local link)
	
	- Start with prefix FE80::/10
	
	- Example:
		- fe80::a2c8:1e56:adfe:25b6
		
- Multicast Address:
	- Multicast addresses are used to send data to a group of devices on the network
	
	- Example:
		- ff02::1 (all nodes on the local link)
		
- Anycast Address:
	- Anycast addresses are assigned to multiple devices, and the packet is delivered to the nearest device (in terms of routing distance)

## IPv6 Addresses Assigned
- Stateless Address Autoconfiguration (SLAAC):
	- What?
		- SLAAC allows devices to automatically configure their own IPv6 address without needing a DHCP server. The device generates its own address based on its MAC address and the network prefix advertised by the router
		
	- Why?
		- Autonomous:
			- Devices can configure themselves without manual intervention or a DHCP server
			
		- Simplifies network:
			- Devices can communicate as soon as they receive Router Advertisements (RAs) from a router
			
	- How?
		- The device sends a Router Solicitation (RS) message to find routers
		
		- The router responds with a Router Advertisement (RA) message, which includes the prefix (network portion of the IPv6 address) and other configuration information
		
		- The device generates its IPv6 address using the prefix from the RA and combines it with a unique identifier (based on the device's MAC address)
		
	- SLACC Example:
		- The router advertises the prefix 2001::0db8:85a3::/64 via Ra
		
		- The device generates an address like 2001:0db8:85a3:0000:0000:8a2e:0370:7334
		
- Stateful DHCPv6:
	- What?
		- Stateful DHCPv6 works similarly to DHCPv5, where a DHCPv6 server assigns IPv6 addresses to devices. The DHCP server keeps track of which addresses have been assigned and to which devices
		
	- Why?
		- Centralized management:
			- Network administrators have full control over address allocation
			
		- No reliance on SLAAC:
			- Some networks may prefer stateful configuration for consistency or because SLAAC doesn't provide other configuration options (like DNS)
			
	- How?
		- The client sends DHCPv6 Request message to the DHCP server
		
		- The DHCP server responds with an IPv6 address and other configuration details (like DNS servers)
		
		- The client uses the provided IPv6 address to communicate on the network

# IPv6 Stateless Address Autoconfiguration (SLAAC) vs Stateful DHCPv6
- SLAAC:
	- The device configures itself using the information provided by the router (via Router Advertisements)
		- Pros:
			- No need for DHCP server, simpler configuration
		- Cons:
			- Limited to address configuration; does not provide DNS or other settings
			
- Stateful DHCPv6:
	- A DHCP server provides the address and configuration (including DNS and more)
		- Pros:
			- Full control over the addressing and configuration process
		- Cons:
			- Requires a DHCPv6 server

## QNA
- **What is the difference between SLAAC and Stateful DHCPv6?**
    
    - **SLAAC** allows devices to **automatically configure** their own **IPv6 address** using the prefix advertised by a router. **Stateful DHCPv6** requires a **DHCP server** to assign an IPv6 address to the device.
        
- **What are the benefits of using SLAAC in an IPv6 network?**
    
    - **Simplicity**: Devices can **self-configure** without requiring a DHCP server.
        
    - **Autonomy**: Devices generate their own **IPv6 address** based on the router's advertised prefix.
        
- **How does SLAAC work to assign an IPv6 address to a device?**
    
    - The device listens for a **Router Advertisement (RA)**, uses the **prefix** in the RA, and appends its own **unique identifier** (often derived from its MAC address) to form the **full IPv6 address**.
    
- **What is the purpose of the "ipv6 dhcp pool" command in DHCPv6 configuration?**

	- The **"ipv6 dhcp pool"** command is used to define the **range of IPv6 addresses** that the router can assign to clients via **DHCPv6**.