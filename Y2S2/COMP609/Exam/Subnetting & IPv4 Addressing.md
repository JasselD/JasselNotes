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
	- It is called "slash notation"
- ANDing proccess:
	- Used to identify the network address by performing a bitwise AND between the IP address and the subnet mask

# Types of IPv4 Addresses
- Network Address
	- Identifies the entire subnet (e.g., 192.168.1.0/24)
	
- Host Addresses
	- Usable IPs within a subnet (e.g., 192.168.1.1 - 192.168.1.254)
	
- Broadcast Address
	- Last address in subnet (e.g., 192.158.1.255)

# Special IPv4 Addresses
- Loopback
	- Range:
		- 127.0.0.1
	- Purpose:
		- Used for internal testing (e.g., pinging self)
		
- Link-local/APIPA
	- Range:
		- 169.254.0.0/16
	- Purpose:
		- Assigned automatically when DHCP fails

# Reasons for subnetting
- Reduces network congestions
- Enchances performance
- Implements security boundaries
- Allows logical groupings (location, department, device type)

# Subnetting Methods
- Subnetting on Octet Boundaries
	- Uses standard subnet sizes:
		- /8, /16, /24
		
- Subnetting Within Octets
	- Use custom mask like /26, /30
	- More control over host allocation

# VLSM (Variable Length Subnet Mask)
- What?
	- VLSM alows for subnetting a subnet using different subnet masks per segment
	- Start with the largest host requirement, then move down
	
- Example Task:
	- Design a VLSM-based IP plan for network 192.168.4.0/24
	
- VLSM helps optimize IP usage

# Short QNA
- **How many bits are in an IPv4 address?**  
    **Answer:** 32 bits
    
- **What is the format of an IPv4 address?**  
    **Answer:** Dotted decimal format (e.g., 192.168.1.1)
    
- **What range does each octet of an IPv4 address fall into?**  
    **Answer:** 0 to 255
    
- **What is the main purpose of a subnet mask?**  
    **Answer:** To distinguish the network portion from the host portion of an IP address
    
- **Which class does the IP address 10.0.0.1 belong to?**  
    **Answer:** Class A
    
- **What is the default subnet mask for Class B?**  
    **Answer:** 255.255.0.0 (/16)
    
- **How many hosts can Class C support per network?**  
    **Answer:** 254 hosts
    
- **What address is used for loopback testing?**  
    **Answer:** 127.0.0.1
    
- **What IP address range is used by APIPA?**  
    **Answer:** 169.254.0.0/16
    
- **What is VLSM used for?**  
    **Answer:** To allocate different subnet sizes based on host requirements, optimizing IP usage

# Long QNA
1. **Explain the structure of an IPv4 address and how the network and host portions are determined.**  
    An IPv4 address is made up of 32 bits divided into four octets, and it is written in a dotted decimal format such as 192.168.1.1. Each octet contains 8 bits and ranges in value from 0 to 255. The address is logically divided into two parts: the network portion and the host portion. The network portion identifies the specific network the device belongs to, while the host portion identifies the individual device on that network. This division is determined using a subnet mask, which is also a 32-bit value where the bits set to 1 indicate the network portion and the bits set to 0 indicate the host portion.
    
2. **Describe the different IPv4 address classes and their uses.**  
    IPv4 addresses are traditionally divided into five classes: A, B, C, D, and E.
    
    - **Class A** addresses start with a 0 bit and range from 1.0.0.0 to 126.255.255.255. They use a default subnet mask of 255.0.0.0 (/8) and can support over 16 million hosts per network, making them suitable for very large organizations like ISPs.
        
    - **Class B** addresses start with 10 and range from 128.0.0.0 to 191.255.255.255. With a default subnet mask of 255.255.0.0 (/16), they support around 65,000 hosts and are used in medium-sized networks like universities.
        
    - **Class C** addresses start with 110 and range from 192.0.0.0 to 223.255.255.255. These have a default subnet mask of 255.255.255.0 (/24) and support 254 hosts per network, ideal for small businesses.
        
    - **Class D** addresses (224.0.0.0 to 239.255.255.255) are reserved for multicast communication.
        
    - **Class E** addresses (240.0.0.0 to 255.255.255.255) are reserved for experimental use and are not used in general networking.
        
3. **What are the benefits of subnetting, and how does VLSM enhance those benefits?**  
    Subnetting allows a larger network to be divided into smaller, more manageable subnetworks. This reduces network congestion, improves performance, enhances security by isolating segments, and enables logical grouping of devices based on factors like department or location. VLSM (Variable Length Subnet Mask) enhances these benefits by allowing different subnet sizes within the same network. Instead of using fixed-size subnets, VLSM lets network administrators allocate addresses more efficiently based on actual host requirements, starting with the largest subnet and working downward. This method avoids IP wastage and makes IP address allocation much more flexible and efficient.
    
4. **What are network, host, and broadcast addresses in IPv4, and how are they determined?**  
    In IPv4, a network address represents the entire subnet and is the first address in the range (e.g., 192.168.1.0 for a /24 subnet). Host addresses are the usable IP addresses within that subnet that can be assigned to individual devices; for a /24 subnet, these range from 192.168.1.1 to 192.168.1.254. The broadcast address is the last address in the subnet (e.g., 192.168.1.255 for a /24), used to send messages to all hosts within that subnet. These addresses are calculated using the IP address and the subnet mask through a bitwise AND operation, known as the ANDing process, which separates the network portion from the host portion.
