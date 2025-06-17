# IPv4 Addressing
- What?
	- IPv4 address ia a 32-bit hierarchical identifier assigned to each device on a network. It's written in dotted decimals format (e.g., 192.168.1.1) and consist of four octets (8 bits each)
	
	- Example IP:
		- 192.168.1.20 = 11000000.10101000.00000001.00010100 (binary)
		- This can be calculated in calculator app
		
	- Each octet ranges from 0 to 255

# IPv4 Structure
- Network Portion:
	- Identifies the network
	
- Host Portion:
	- Identifies the devices within that network
	
- Determined using the Subnet Mask

# IPv4 Address Classes (A, B, C)
- IPv4 addresses are traditionally grouped into classes to help define how many networks and hosts per network are possible
- Class A:
	- Starting Bits:
		- 0xxx
	- IP Range:
		-   1.0.0.0 - 126.255.255.255
	- Default Subnet Mark:
		- 255.0.0.0 (/8)
	- Host per Network
		- 16.7 million
	- Use Case:
		- Very large networks (ISPs, multinational corps)
- Class B:
	- Starting Bits:
		- 10xx
	- IP Range:
		-   128.0.0.0 - 191.255.255.255
	- Default Subnet Mark:
		- 255.255.0.0 (/16)
	- Host per Network
		- 65000
	- Use Case:
		- Medium-sized networks (Universities, companies)
		
- Class C:
	- Starting Bits:
		- 110x
	- IP Range:
		-   192.0.0.0 - 223.255.255.255
	- Default Subnet Mark:
		- 255.255.255.0 (/24)
	- Host per Network
		- 254
	- Use Case:
		- Small networks (offices, small businesses)
		
- 127.0.0.0/8 is reserved for loopback
- 224.0.0.0 - 239.255.255.255 is Class D (Multicast)
- 240.0.0.0 - 255.255.255.255 is Class E (Experimental)

# Subnet Mask
- Subnet mask is used to determine which part of the IP address is the network and which is the host
- Subnet Mask:
	- 255.0.0.0 
		- /8 
	- 255.255.0.0 
		- /16 
	- 255.255.255.0
		- /24 
- Prefix length:
	- The number of bits set to 1 in subnet mask
	- 
