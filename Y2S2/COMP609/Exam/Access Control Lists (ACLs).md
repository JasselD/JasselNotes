# ACL
-  An Access Controls List (ACL) is a set of rules used by routers or firewalls to control incoming and outgoing network traffic
- Each rule defines whether to permit or deny packets based on various criteria like:
	- IP address
	- Protocol type
	- Port Number
	- Source/destination
- Think of ACLs as digital traffic cops filtering which data gets through

# Types of ACLs
- Standard ACL:
	- Filters traffic based only on source IP address
	- Granularity:
		- Basic
- Extended ACL:
	- Filters traffic based on source and destination IP, protocol, and ports
	- Granularity:
		- Detailed

# Example ACL Commands
- Standard ACL
```bash

access-list 1 permit 192.168.1.0 0.0.0.255
interface g0/1
ip access-group 1 in
```
- Permits access from 192.168.1.0/24 network

- Extended ACL
```bash

access-list 100 deny tcp 192.168.1.0 0.0.0.255 any eq 80
access-list 100 permit ip any any
interface g0/0
ip access-group 100 in
```

# Tips & Rules
- ACLs are processed top-down, first match wins
- An implicit deny all exists at the end of every ACL
- Use access-list numbers:
	- 1-99 = Standard
	- 100-199 = Extended

# Short QNA
1. **What does ACL stand for in networking?**  
    ACL stands for **Access Control List**.
    
2. **What is the primary purpose of an ACL?**  
    The primary purpose of an ACL is to **filter network traffic** by allowing or denying packets based on criteria such as IP address, protocol type, and port numbers.
    
3. **What criteria can be used in an ACL to permit or deny traffic?**  
    An ACL can filter traffic based on **IP address**, **protocol type**, **port number**, and **source or destination information**.
    
4. **What type of ACL filters traffic using only the source IP address?**  
    A **Standard ACL** filters traffic based **only on the source IP address**.
    
5. **What type of ACL can filter by source, destination, protocol, and ports?**  
    An **Extended ACL** can filter traffic by **source and destination IP addresses, protocol types, and port numbers**.
    
6. **In what order are ACL rules processed?**  
    ACL rules are processed in a **top-down** order, and the **first match is applied**.
    
7. **What is the significance of the implicit deny statement in ACLs?**  
    Every ACL has an **implicit “deny all”** at the end, which means any packet not explicitly permitted will be denied by default.
    
8. **What is the number range for standard and extended ACLs?**  
    **Standard ACLs** use numbers **1–99**, while **Extended ACLs** use numbers **100–199**.
    
9. **What does the command `access-list 1 permit 192.168.1.0 0.0.0.255` do?**  
    This command **permits traffic** from the **192.168.1.0/24** network.
    
10. **What does the command `access-list 100 deny tcp 192.168.1.0 0.0.0.255 any eq 80` do?**  
    This command **denies TCP traffic** from the **192.168.1.0/24 network** to **any destination on port 80 (HTTP)**.

# Long QNA
- **What is an Access Control List (ACL) and how does it work in a network?**  
    An **Access Control List (ACL)** is a set of rules applied to a router or firewall that controls **which packets are allowed or denied** as they enter or exit a network interface. Each rule, or statement, is evaluated in order from top to bottom, and once a match is found, the corresponding action (permit or deny) is applied. ACLs help enforce security policies by filtering traffic based on IP addresses, protocols, and port numbers.
    
- **Compare Standard and Extended ACLs in terms of filtering capabilities and use cases.**  
    **Standard ACLs** offer basic filtering by checking only the **source IP address** of incoming packets. They are simpler and best used **close to the destination** to reduce unnecessary filtering early in the network.  
    **Extended ACLs**, on the other hand, provide **granular filtering** by examining both **source and destination IP addresses**, **protocol types**, and **port numbers**. They are suitable for **precise traffic control** and are usually placed **close to the source** of the traffic to prevent unwanted data from entering the network in the first place.
    
- **Explain how ACLs are processed and why the order of rules is important.**  
    ACLs are processed in a **top-down sequence**, meaning the router or firewall evaluates each rule in the order it appears in the list. The first rule that matches a packet’s criteria determines the action taken, and the packet is not checked against any remaining rules. Additionally, all ACLs end with an **implicit deny all**, so any packet not explicitly permitted will be dropped. Therefore, the **order of the rules is critical**—placing more specific rules before general ones ensures that important traffic is properly filtered.
    
- **Describe a scenario where you would use an extended ACL to block specific traffic.**  
    Imagine you have a web server connected to your internal network, and you want to **block HTTP traffic (port 80)** from a specific subnet (192.168.1.0/24) for security reasons. You could use the command:
    
    pgsql
    
    CopyEdit
    
    `access-list 100 deny tcp 192.168.1.0 0.0.0.255 any eq 80   access-list 100 permit ip any any`
    
    This extended ACL denies all HTTP requests from that subnet while allowing all other traffic. You would apply this ACL inbound on the interface receiving traffic from that subnet. This use of an **extended ACL** allows for **fine-grained control** over specific types of traffic.
    
- **Why is the implicit deny in ACLs important, and how can it cause unintended issues?**  
    The **implicit deny all** at the end of every ACL means that if a packet does not match any of the listed rules, it will be **automatically denied**. This is important for security because it ensures that no unapproved traffic slips through. However, if administrators **forget to include a final “permit” rule** or incorrectly order the rules, legitimate traffic may be unintentionally blocked. Therefore, it is essential to carefully plan and test ACL configurations to avoid **unintended service disruptions**.