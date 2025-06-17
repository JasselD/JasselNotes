# DHCP
- What?
	- DHCP is a network protocol that automatically assigns IP addresses and other network configuration parameters (like default gateway, subnet mask, and DNS) to devices on a network. Instead of manual configuration, clients receive IP details dynamically from a DHCP server

# DHCP Lease Acquisition Process
- **DORA**
	- Discover:
		- Clients sends a broadcast to find DHCP sercer
		- "Is anyone out there?"
		
	- Offer:
		- Server responds with an IP offer and configuration
		- "Here's an IP you can use"
		
	- Request:
		- Clients requests the offered IP
		- "I'd like this one, please"
		
	- ACK:
		- Server acknowledges the request
		- "It's all yours"

# DHCP Lease Renewal Process
- Renewal (T1):
	- When 50% of the lease time has passed, the client sends a DHCPREQUEST to renew
	
- Rebinding (T2):
	- At 87.5% of lease time, the client tries any DHCP server if no response
	
- Lease Expiry:
	- If no DHCP server responds, the IP address lease expires, and the client must restart the DORA process

## When DHCP Fails
- APIPA/Link-local address (169.254.x.x) is assigned automatically by the client if DHCP is unreachable


# Short QNA
- **What does DHCP stand for?**  
    **Answer:** Dynamic Host Configuration Protocol
    
- **What is the main function of DHCP?**  
    **Answer:** To automatically assign IP addresses and network configuration settings to devices on a network.
    
- **What does DORA stand for in DHCP?**  
    **Answer:** Discover, Offer, Request, Acknowledge
    
- **What happens during the 'Offer' stage of DORA?**  
    **Answer:** The DHCP server responds with an IP address offer and configuration details.
    
- **At what percentage of the lease time does the DHCP client attempt to renew the lease?**  
    **Answer:** At 50% of the lease time (T1).
    
- **What IP range is assigned if DHCP fails?**  
    **Answer:** 169.254.x.x (APIPA/Link-local address)
    
- **What happens at 87.5% of the lease time?**  
    **Answer:** The client enters the rebinding phase and tries to contact any DHCP server.
    
- **What happens if a DHCP lease fully expires without renewal?**  
    **Answer:** The client restarts the DORA process to obtain a new lease.

# Long QNA
- **Explain the DORA process in DHCP lease acquisition.**  
    **Answer:**  
    The DORA process is the four-step method used by a client to obtain an IP address from a DHCP server:
    
    - **Discover:** The client broadcasts a DHCPDISCOVER message to find available DHCP servers on the network.
        
    - **Offer:** A DHCP server responds with a DHCPOFFER, which includes an available IP address and configuration details.
        
    - **Request:** The client replies with a DHCPREQUEST to accept the offer and formally request the IP.
        
    - **Acknowledge:** The server sends a DHCPACK to confirm the lease, and the client can now use the assigned IP address.
        
- **Describe what happens during the DHCP lease renewal and what actions the client takes if renewal fails.**  
    **Answer:**  
    After obtaining an IP address, the client monitors the lease duration:
    
    - At **50%** of the lease time (T1), the client tries to **renew** the lease directly with the original DHCP server by sending a DHCPREQUEST.
        
    - If no response is received, at **87.5%** of the lease time (T2), the client enters the **rebinding** state and broadcasts a request to **any** available DHCP server.
        
    - If there is still no response by the lease **expiry**, the client **loses its IP** and must restart the **DORA** process to obtain a new lease.
        
- **What is APIPA, and when is it used?**  
    **Answer:**  
    APIPA (Automatic Private IP Addressing), also known as Link-local addressing, assigns an IP address from the **169.254.x.x** range to a device when it cannot contact a DHCP server. This allows limited local communication within the same subnet but **does not allow Internet access**. It is used as a fallback mechanism when DHCP fails.
