- What?
	- <mark style="background: #ABF7F7A6;">Logical grouping of devices</mark> in a network, regardless of their physical locations. Devices in the <mark style="background: #ABF7F7A6;">same VLAN can communicate directly with each other</mark>, while devices in <mark style="background: #ABF7F7A6;">different VLANs cannot communicate unless routed by a router or Layer 3 switch</mark>
- Why?
	- <mark style="background: #ABF7F7A6;">Segmentation</mark>:
		- VLANs divide a large broadcast domain into <mark style="background: #ABF7F7A6;">smaller, isolated broadcast domains</mark>. This helps <mark style="background: #ABF7F7A6;">reduce broadcast traffic</mark> and <mark style="background: #ABF7F7A6;">improves network performance</mark>
		- <mark style="background: #ABF7F7A6;">Security</mark>:
			- VLANs provide a <mark style="background: #ABF7F7A6;">logical separation of devices</mark>. For example, finance devices can be in one VLAN, and HR devices can be in another, increasing security by limiting access
		- <mark style="background: #ABF7F7A6;">Simplified Management</mark>:
			- VLANs <mark style="background: #ABF7F7A6;">allow network administrators to group devices by function</mark>, even if they're spread across different physical location. This makes <mark style="background: #ABF7F7A6;">management easier and more efficient</mark>
- How?
	- <mark style="background: #ABF7F7A6;">VLAN Tagging</mark>:
		- When device sends data, it is assigned a VLAN ID. This ID is added to the frame by the switch to tag the traffic as beloging to a specific VLAN
		- <mark style="background: #ABF7F7A6;">Trunk Links</mark> between switches use <mark style="background: #ABF7F7A6;">802.1Q VLAN tagging</mark> to allow traffic from <mark style="background: #ABF7F7A6;">multiple VLANs to pass through a single physical link</mark>
	- Switch Port Modes:
		- A switch port can be in one of the following modes:
			- <mark style="background: #ABF7F7A6;">Access Mode</mark>:
				- The port is assigned to a <mark style="background: #ABF7F7A6;">single VLAN</mark>. Devices connected to the port are part of the VLAN
			- <mark style="background: #ABF7F7A6;">Trunk Mode</mark>:
				- THe port can carry traffic from <mark style="background: #ABF7F7A6;">multiple VLANs</mark> and tags each frame with the appropriate VLAN ID

**VLAN Routing**
- Allow <mark style="background: #ABF7F7A6;">communication between devices in different VLANs</mark>, you need to <mark style="background: #ABF7F7A6;">configure inter-VLAN routing</mark>. This can be done using a <mark style="background: #ABF7F7A6;">router</mark> or a <mark style="background: #ABF7F7A6;">Layer 3 switch</mark>
- <mark style="background: #ABF7F7A6;">Router-on-a-stick</mark>:
	- This method involves <mark style="background: #ABF7F7A6;">creating subinterfaces on a router</mark>, each associated with a specific VLAN

**<mark style="background: #ABF7F7A6;">QNA</mark>
- What is the main purpose of VLANs in a network?
	- The main purpose of VLANs is to **segregate** devices into **logical groups** regardless of their physical location, improving **network performance** by reducing **broadcast traffic** and increasing **security** by isolating different groups of devices.
	
- What does VLAN tagging do in a network?
	- **VLAN tagging** adds a **VLAN ID** to frames as they travel through **trunk links** between switches, allowing **multiple VLANs** to share a single physical link while keeping traffic from each VLAN separate.
	
- What are the two main types of switch port modes?
	- **Access Mode**: The port is assigned to a single VLAN.
    - **Trunk Mode**: The port can carry traffic from multiple VLANs and tags each frame with the appropriate VLAN ID.
    
- What is the purpose of inter-VLAN routing?
	- **Inter-VLAN routing** allows devices in different VLANs to **communicate** with each other. This is achieved by a **router** or a **Layer 3 switch** that routes traffic between VLANs.