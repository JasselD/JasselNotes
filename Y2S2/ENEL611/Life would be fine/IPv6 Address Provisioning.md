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
	- Anycast addresses are assigned to multiple devices, and the packet is delivered to the nearest device (in terms of routing )