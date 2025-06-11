# EtherChannel
- What?
	- EtherChannel is a link aggregation technology that allows you to bundle multiple physical Ethernet links between devices (such as switches or a switch and a server) into a single logical link
	
	- Used to increase bandwidth and provide redundancy by ensuring that if one link fails, the others will still carry traffic, ensuring network resiliency
	
- Why?
	- Increase Bandwdith:
		- Instead of having a single 1Gbps link between switches, you can combine multiple links (e.g, 2x 1Gbps links) to create a 2Gbps link
		
	- Redundancy:
		- If one physical link fails, the traffic will automatically be forwarded over the other active links, ensuring no discruption in service
		
	- Simplified Configuration:
		- EtherChannel simplifies network configuration by creating a single logical interface that behaves like a single link, even though multiple physical links are involved
		
- How?
	- Link Aggregation:
		- EtherChannel groups several physical links (Ethernet ports) into one logical link. This is done using the LACP (Link Aggregation Control Protocol) or PAgP (Port Aggregation Protocol)
		
	- Load Balancing:
		- EtherChannel distributes traffic over the multiple physical links, improving bandwidth and preventing any single link from becoming overwhelmed
		
	- Protocol Support:
		- EtherChannel can use LACP (open standard) or PAgP (Cisco proprietary) to negotiate link bundling

## 