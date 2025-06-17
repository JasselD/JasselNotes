# DNS
- What?
	- DNS is like the Internet's phonebook. It translate human-readable hostnames into IP addressess that computer use to locate each other

# DNS concepts & Structure
- Hostname:
	- The human-readable name of a device on a network
		- www.example.com
		
- Namespace:
	- The structured naming hierarchy that organizes domain names. Root -> Top-level Domains (TLD) -> Domains -> Subdomains
	
- Record Types:
	- DNS stores data in records (A, AAAA, CNAME, MX, etc.)

# DNS Query Types
- Recursive Query:
	- Clients asks DNS server to resolve the full IP; server takes responsibility to complete the process
- Iterative Query:
	- DNS server gives the clients the best answer it has and refers it to another DNS server to conti