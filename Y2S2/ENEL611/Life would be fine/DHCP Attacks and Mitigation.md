# DHCP Attacks
- What?
	- Occurs when a malicious device or user manipulates or exploits the DHCP process to disrupt or gain unauthorized access to the network
	- Common types of DHCP attacks:
		- DHCP Spoofing:
			- What?
				- An attacks impersonates a DHCP server and sends fake DHCP responses to clients. This can result in clients receiving incorrect IP addresses, default gateways, and DNS servers, potentially redirecting traffic or causing network outages
				
			- Why?
				- Attacker can control client configurations, leading to network disruption or data interception (main-in-the middle attack)
				
		- Rogue DHCP Servers:
			- What?
				- Rogue DHCP server is an unauthorized DHCP server that operates on the network. It can interface with the legitimate DHCP process, leading to incorrect IP assignments or network outages
				
			- Why?
				- Rogue servers can provide incorrect network configurations to clients or cause IP address conflicts
				
		- DHCP Starvation:
			- What?
				- DHCP starvation attack, an attacker sends a large number of DHCP requests to exhaust the DHCP pool of available IP addresses. This causes legitimate devices to be unable to obtain an IP address from the DHCP server
				
			- Why?
				- This attack can cause Denial of Service (Dos), preventing users from connecting to the network

# Mitigating DHCP Attacks
- Techniques used to mitigate DHCP attacks:
	- DHCP Snooping