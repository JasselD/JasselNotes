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
	- DNS server gives the clients the best answer it has and refers it to another DNS server to continue the query

# DNS Lookup Process (Simplified)
1. User types www.example.com
2. Local DNS Resolver checks its cache
3. If not found, it contacts Root DNS Server
4. Root refers to TLD DNS Server (e.g., .com)
5. TLD DNS refers to Authoritative DNS Server
6. IP address is returned -> Browser loads website

# Short QNA
- **What does DNS stand for and what is its primary function?**  
    ➤ _Domain Name System; it translates human-readable hostnames into IP addresses._
    
- **What is a hostname?**  
    ➤ _A human-readable name of a device on a network, like [www.example.com](http://www.example.com)._
    
- **What is the DNS namespace structure?**  
    ➤ _It is a hierarchy: Root → Top-level Domains (TLDs) → Domains → Subdomains._
    
- **Name two common DNS record types.**  
    ➤ _A (IPv4 address), CNAME (canonical name)._
    
- **What is the difference between a recursive and an iterative DNS query?**  
    ➤ _A recursive query makes the DNS server resolve the full IP address, while an iterative query gets referred step-by-step to other DNS servers._

# Long QNA
- **Explain the process of DNS lookup from the moment a user types a website into the browser.**  
    ➤ _When a user types a URL like [www.example.com](http://www.example.com), the local DNS resolver first checks its cache. If not found, it sends a query to the Root DNS server. The Root server points to the appropriate TLD server (like .com), which in turn points to the authoritative DNS server for the domain. That server provides the IP address, and the browser uses it to load the website._
    
- **Compare and contrast recursive and iterative DNS queries with an example.**  
    ➤ _In a recursive query, the DNS server takes full responsibility to fetch the IP and return it to the client—like a concierge who does all the work. For example, your local DNS resolver handles everything and gives you the final IP. In an iterative query, the server only gives the next step (e.g., "Go ask that other server"), so the client must follow up with each server in the chain._
    
- **Describe the DNS namespace and why it's important.**  
    ➤ _The DNS namespace is a hierarchical structure that organizes domain names. It starts from the root (.), branches into TLDs like .com or .org, then into individual domains like example.com, and further into subdomains like [www.example.com](http://www.example.com). This structured approach ensures global uniqueness and scalability across billions of internet-connected devices._
