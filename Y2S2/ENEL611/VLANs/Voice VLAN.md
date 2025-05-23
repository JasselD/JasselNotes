**Voice VLAN**
- Voice VLAN is a dedicated VLAN created specifically to carry Voice over IP (VoIP) traffic
- VoIP traffic needs special treatment to maintain good call quality
- VoIP Traffic Requirements:
	- Assured Bandwidth:
		- To prevent dropped or choppy calls
	- Transmission Priority:
		- Voice traffic must be prioritised over data traffic
	- Routing Flexibility:
		- Able to avoid congested paths
	- Low Delay:
		- Network delay must be less than 150 ms end-to-end
- Purpose:
	- A Voice VLAN ensures:
		- Better voice quality
		- Less interference from normal data traffic
	- The switch must be properly configured to:
		- Separate voice traffic from regular data traffic
		- Prioritise voice frames using QoS (Quality of Service)
- Example:
	- VLAN 150 = Voice VLAN (For Cisco IP phones)
	- VLAN 20 = Data VLAN (for student's computer, PC5)
	- Setup:
		- PC5 connects to the IP phone
		- The IP phone connects to the switch (S3)
		- The IP phones tags voice traffic into VLAN 150 and forwards PC4's data traffic into VLAN 20

![[Pasted image 20250428180607.png]]
