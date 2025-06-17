# DHCP
- What?
	- DHCP is a network protocol that automatically assigns IP addresses and other network configuration parameters (like default gateway, subnet mask, and DNS) to devices on a network. Instead of manual configuration, clients receive IP details dynamically from a DHCP server

# DHCP Lease Acquisition Process
- **DORA**
	- Discover:
		- Clients sends a broadcast to find DHCP sercer
		- "Is anyone out there?"
		
	- Offer:
		- Server responds with an IP offer and configuration
		- "Here's an IP you can use"
		
	- Request:
		- Clients requests the offered IP
		- "I'd like this one, please"
		
	- ACK:
		- Server acknowledges the request
		- "It's all yours"

# DHCP Lease Renewal Process
- Renewal (T1):
	- When 50% of the lease time has passed, the client sends a DHCPREQUEST to renew
	
- Rebinding (T2):
	- At 87.5% of lease time, the client tries any DHCP server if no response
	
- Lease Expiry:
	- If no DHCP server responds, the IP address lease expires, and the client must restart the DORA process

## When DHCP Fails
- APIPA/

