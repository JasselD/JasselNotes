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
- ``
```