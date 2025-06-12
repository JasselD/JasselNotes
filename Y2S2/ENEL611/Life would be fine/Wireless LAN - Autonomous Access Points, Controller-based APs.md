# Access Point (AP)
- What?
	- A device that allows wireless devices to connect to a wired network. APs typically connect to a wired LAN and provide Wi-Fi connectivity for devices like laptops, smartphones, and tablets

# Autonomous Access Points (Standalone APs)
- What?
	- Autonomous APs are the standalone devices that function independently. Each AP has its own configuration interface and operates as a self-contained unit. This means that every AP needs to be configured individually
	
- Why?
	- Simpler Networks:
		- Ideal for small or medium-sized networks where the number of APs is limited and manual configuration is feasible
		
	- Local Configuration:
		- Each AP is configured separately, which gives network administrators direct control over each device
		
- How?
	- They broadcast a single SSID (Service Set Identifier) and handle authentication, encryption, and traffic forwarding locally
	
	- They can support multiple SSIDs and VLANs

# Controller-based Access Points (Controller-managed APs)
- What?
	- Controller-based APs are managed by a central controller (called a Wireless LAN Controller or WLC). This allows centralized management of all APs in the network
- Why?
	- Scalable Networks:
		- Ideal for large networks where managing each AP individually would be impractical. Controller-based systems allow for easier deployment and management of multiple APs
		
	- Centralized Management:
		- Configuration and management of all APs are handled centrally through the WLC, making it easier to configure, monitor, and troubleshoot the network
		
- How?
	- The controller communicates with each AP, pushing configuration settings like SSID settings, security policies, and firmware updates
	
	- Each AP is dependent on the controller for configuration, which simplifies the deployment and management process
	
- Benefits:
	- Seamless Roaming:
		- As devices move between APs, the controller ensures continous connectivity by managing the handoff between APs
		
	- Enchanced Security:
		- Centralized management allows for consistent security policies across all APs
		
	- Load Balancing:
		- The controller can balance the load between multiple APs, ensuring optimal network performance

## Choosing Between Autonomous and Controller-based APs
- Autonomous APs
	- Suitable for small to medium-sized networks with a limited number of devices and APs
	
	- Offer lower initial cost but may require more manual management as the network grows
	
- Controller-based APs
	- More suited for large-scale networks, where centralized management, seamless roaming, and scalability are critical
	
	- Require additional infrastructure (WLC) but provide better manageability in the long run

## QNA
- **What is the main difference between Autonomous APs and Controller-based APs?**
    
    - **Autonomous APs** are standalone devices that are **individually managed**, while **Controller-based APs** are managed by a **central Wireless LAN Controller (WLC)**, allowing **centralized management** of the network.
        
- **Why would you choose Autonomous APs for a network?**
    
    - **Autonomous APs** are ideal for **small to medium-sized networks** where **manual configuration** is feasible and there is no need for centralized management.
        
- **How do Controller-based APs provide seamless roaming?**
    
    - Controller-based APs enable **seamless roaming** by allowing the **controller** to manage the handoff process between APs as users move around the network. The controller ensures that the device stays connected without dropping the connection.
        
- **What are the advantages of using Controller-based APs in a large network?**
    
    - **Controller-based APs** provide **centralized management**, **easier scalability**, **seamless roaming**, **consistent security policies**, and **automatic firmware updates**, making them ideal for large networks.
        
- **How are security settings handled in Autonomous APs compared to Controller-based APs?**
    
    - **Autonomous APs** require **individual configuration** of security settings on each AP. In **Controller-based APs**, security settings are **configured centrally** through the WLC and applied to all APs in the network.