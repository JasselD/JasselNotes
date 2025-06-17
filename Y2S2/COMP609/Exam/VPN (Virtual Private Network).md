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
	- The entire IP packet is encrypted, then encapsulated in a new IP packet. Common in site-to-site VPNs

# VPN Protocols
- IPsec:
	- Industry standard for secure VPN tunnels(supports both transport and tunnel modes)
	
- PPTP (obsolete):
	- Older and less secure
	
- L2TP + IPsec:
	- Combines features of Layer 2 Tunneling and IPsec encryption
	
- SSL VPN:
	- Commonly used in web browsers for remote access
	
- OpenVPN:
	- Open-source, very secure, uses TLS for encryption

# Uses Cases
- Remote Work:
	- Secure access to company resources
	
- Travelling Employees:
	- Connect securely to home network from public Wi-Fi
	
- Site-to-Site VPNs:
	- Connect branch offices securely

# Short QNA
- **What does VPN stand for?**  
    VPN stands for **Virtual Private Network**.
    
- **What is the main purpose of a VPN?**  
    A VPN creates a **secure, encrypted tunnel** that allows devices to connect to a private network over a public network, ensuring confidentiality, integrity, and authentication of data.
    
- **What component of a VPN encapsulates and encrypts data?**  
    The **tunneling protocol** is the component that encapsulates and encrypts data between networks.
    
- **What is the role of authentication in a VPN?**  
    **Authentication** verifies the identity of the connecting device or user to ensure that only authorized access is allowed.
    
- **Which VPN mode encrypts only the data payload, not the IP headers?**  
    **Transport mode** encrypts only the payload, leaving the IP headers visible.
    
- **Which VPN mode encrypts the entire IP packet?**  
    **Tunnel mode** encrypts the entire IP packet and wraps it in a new one, making it ideal for site-to-site VPNs.
    
- **What is IPsec used for in VPNs?**  
    **IPsec** is used to create secure VPN tunnels and supports both transport and tunnel modes.
    
- **Which VPN protocol is open-source and uses TLS for encryption?**  
    **OpenVPN** is open-source and uses **TLS (Transport Layer Security)** to encrypt traffic.
    
- **Why is PPTP considered obsolete?**  
    **PPTP** is considered obsolete because it has known security vulnerabilities and is no longer recommended for secure communication.
    
- **What is a common use case for SSL VPNs?**  
    **SSL VPNs** are commonly used for **remote access** via web browsers, allowing users to connect securely without specialized software.

# Long QNA
1. **Explain what a VPN is and how it secures communication over the internet.**  
    A **Virtual Private Network (VPN)** is a technology that creates a secure tunnel between a device and a private network over the internet. It **encrypts data** to prevent eavesdropping, **authenticates** users to ensure only authorized access, and **encapsulates** traffic using tunneling protocols. This ensures that even if data travels over public infrastructure, it remains protected from interception and tampering.
    
2. **Compare VPN Transport Mode and Tunnel Mode. When is each used?**  
    **Transport mode** encrypts only the data (payload) of each packet, leaving the IP header intact. It is typically used for **end-to-end communication** between hosts.  
    **Tunnel mode**, on the other hand, encrypts the entire original IP packet—including headers—and encapsulates it in a new IP packet. This mode is commonly used in **site-to-site VPNs**, where secure connections are needed between networks rather than individual devices.
    
3. **Describe the core components of a VPN and their functions.**  
    A VPN has three core components:
    
    - **Tunneling Protocol:** This encapsulates and transports the data securely across public networks.
        
    - **Authentication:** This verifies the identity of users or devices attempting to connect to the VPN.
        
    - **Encryption:** This protects the data in transit from being read by unauthorized parties, ensuring confidentiality and integrity.
        
4. **List and describe four common VPN protocols.**
    
    - **IPsec:** An industry-standard protocol that provides strong security and supports both transport and tunnel modes.
        
    - **PPTP:** One of the earliest VPN protocols, now considered obsolete due to its weak encryption.
        
    - **L2TP/IPsec:** A combination of Layer 2 Tunneling Protocol and IPsec, offering better security and encapsulation than PPTP.
        
    - **SSL VPN:** Uses Secure Sockets Layer encryption and is accessible via standard web browsers for remote access.
        
    - **OpenVPN:** A modern, open-source protocol that uses TLS for encryption and is known for its security and flexibility.
        
5. **What are the practical uses of VPNs in real-world scenarios?**  
    VPNs are used in several real-world situations to enhance privacy and secure communications.
    
    - In **remote work**, VPNs allow employees to securely access internal company resources from home or while traveling.
        
    - **Travelling employees** use VPNs to safely connect to their home network or corporate environment when using public Wi-Fi.
        
    - **Site-to-site VPNs** connect entire office networks across different locations, enabling secure communication between branch offices as if they were on the same local network.
- 


