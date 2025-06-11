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
	- DHCP Snooping:
		- What?
			- DHCP Snooping is a security feature that acts as a filter for DHCP messages. It monitors DHCP traffic on the network and ensures that only trusted DHCP servers can provide IP addresses to clients
			
		- How?
			- When enabled, DHCP Snooping ensures that only trusted ports (where DHCP servers are located) can send DHCP offers. Untrusted ports (where clients are connected) will block any DHCP offers from unauthorized servers
			
		- Benefits:
			- Block unauthorized DHCP servers
			- Prevents DHCP spoofing attacks
			
	- DHCP Snooping Binding Database:
		- What?
			- The binding database stores information about IP-to-MAC address mappings, VLANs, and leased IP addresses from DHCP servers
			
			- It is used to track which devices received which IP address from the DHCP server
			
		- Why?
			- The binding database helps to identify any rogue devices attempting to interfere with the legitimate DHCP process
			
	- Port Security:
		- What?
			- Port security helps mitigate DHCP starvation attacks by limiting the number of MAC addresses on a switch port. This can prevent attackers from flooding the DHCP server with fake request
			
	- Dynamic ARP Inspection (DAI):
		- What?
			- DAI prevents ARP spoofing attacks by ensuring that ARP requests and responses are valid. DAI uses the DHCP snooping bindng database to verify that sender's MAC address matches the IP address

## Other DHCP Security Considerations
- DHCP Filtering:
	- Ensures that only authorized DHCP servers can operate on the network. You can configure the switch to allow only trusted DHCP servers or specific DHCP servers based on IP address or MAC address
	
- Rogue DHCP Server Detection
	- What?
		- This feature allows you to detect unauthorized DHCP servers on the network and alert administrators

## QNA
- What is DHCP Spoofing, and how does it affect the network?
	-  **DHCP Spoofing** occurs when an attacker impersonates a DHCP server and sends false DHCP responses to clients. This can lead to clients receiving incorrect IP configurations, causing network disruptions or allowing attackers to intercept traffic.
	
- What is DHCP Snooping, and how does it mitigate DHCP attacks?
	-  **DHCP Snooping** is a security feature that prevents unauthorized DHCP servers from providing IP addresses to clients. It ensures only **trusted ports** (connected to authorized DHCP servers) can send DHCP offers.
	
- How can DHCP Snooping help prevent DHCP Spoofing attacks?
	- **DHCP Snooping** blocks DHCP responses from **untrusted ports** (ports connected to clients) and only allows **trusted ports** (where the DHCP server is located) to send DHCP offers, preventing **DHCP Spoofing**.
	
- What is the purpose of the DHCP binding database?
	- The **DHCP binding database** stores information about IP-to-MAC address mappings, VLANs, and DHCP leases. It is used to **verify** legitimate DHCP clients and ensure correct IP address assignments.
	
- What does the "ip dhcp snooping trust" command do on a switch?
	- The **"ip dhcp snooping trust"** command marks a port as **trusted**, meaning the DHCP server on that port is **authorized** to send DHCP messages to clients. It is typically used for **DHCP server ports**.