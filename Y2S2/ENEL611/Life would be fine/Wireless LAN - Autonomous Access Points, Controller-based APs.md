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
	- Each AP is dependent on the controller for configuration, which