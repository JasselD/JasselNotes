- What?
	- IPv4 addressing assigns unique 32-bits addresses to devices on a network. It's used to identify devices in Layer 3 (Network Layer)
	- Provisioning is the process of assigning these addresses to devices in a network, either manually (static assignment) or automatically (dynamic assignment via DHCP)

## Static IPv4 Address Assignment
- What?
	- Static IP addressing is when you manually configure a fixed IP address on a device. This means that the device will always use the same IP address every time it connects to the network
	- It's ideal for servers, printers, and devices that need a consistent address
	
- Why?
	- Fixed address for critical devices (routers, web servers)
	- Predictability:
		- You always know the address of key devices
		
- How to configure
	- On a router or PC, you configure the IP address, subnet mask, and default gateway

## Dynamic IPv4 Address Assignments (DHCP)
- What?
	- Dynamic Host Configuration Protocol (DHCP) automatically assigns IP addresses to devices when they connect to the network. The DHCP server manages and assigns IP addresses from a pool of available addresses
	
- Why?
	- Automation:
		- Devices automatically receive an IP address, subnet mask, and default gateway without manual configuration
		
	- Scalability:
		- Easier to manage IP addresses in larger networks, as DHCP dynamically assigns and renew addresses
		
	- IP Address Reuse:
		- DHCP and recycle IP addresses when devices disconnect, making efficient use of the address pool
		
- How?
	- DHCP Discover:
		- The client device sends a DHCP Discover message to fing a DHCP server
		
	- DHCP Offer:
		- The server responds with a DHCP Offer, offering an IP address from the pool
		
	- DHCP Request:
		- The client sends a DHCP Request to confirm the offer
		
	- DHCP Acknowledgement:
		- The server sends a DHCP Acknowledgement to finalize the lease and assign the IP

## DHCP Lease Process
- What?
	- A DHCP lease is the period of time that a device is allowed to use a DHCP-assigned IP address. After the lease expires, the device may need to request a new IP address from the DHCP server
	
- Lease Renewal:
	- DHCP clients attempt to renew their lease halfway through the lease time ensure they don't lose connectivity
	
- DHCP Lease Time:
	- You can configure the lease time to determine how long an IP address will be assigned to a client before it must renew

## QNA
- What is the difference between static and dynamic IP addressing?
	- **Static IP addressing** requires **manual configuration** of an IP address on each device. The device always uses the same IP address.
    
	- **Dynamic IP addressing** uses **DHCP** to automatically assign IP addresses to devices when they connect to the network.
	
- How does the DHCP lease process work?
	- The **client** sends a **DHCP Discover** message, the **server** replies with a **DHCP Offer**, the **client** sends a **DHCP Request**, and the **server** responds with a **DHCP Acknowledgment** to finalize the lease.
	
- What is the purpose of a DHCP pool?
	- A **DHCP pool** is a range of **IP addresses** that the DHCP server uses to assign addresses to devices on the network.
