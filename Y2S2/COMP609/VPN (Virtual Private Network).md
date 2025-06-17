# VPN
- What?
	- A secure communication tunnel that allows devices to connect to a private network over a public network (like the internet). It ensures confidentiality, integrity, and authentication of transmitted data
	- Think of it as a secure "tunnel" where all data is encrypted and protected from eavesdroppers

# VPN Core Components
- Tunneling Protocol:
	- Encapsulates and encrypts data between networks
	
- Authentication:
	- Confirms identity of the connecting device/user
	
- Encryption:
	- Protects data during transit

# VPN Modes
- Transport Mode:
	- Only the data (payload) is encrypted, IP headers remain visible. Used between end host
- Tunnel Mode:
	- The entire IP packet is encrypted, then encapsulated in a new IP packet. Commo