**Step 1: Configure the Management Interface**
- In VLAN interface configuration mode, apply an IPv4 address and subnet mask to the management SVI.
- Example: SVI VLAN 99 is assigned:
    - IPv4 address: 172.17.99.11/24
    - IPv6 address: 2001:db8:acad:99::1/64
- The SVI for VLAN 99 will appear as "up/up" once:
    - VLAN 99 is created.
    - A device is connected to a port in VLAN 99.
- For IPv6 configuration on a Cisco Catalyst 2960 with IOS version 15.0:
    - Enter the command `sdm prefer dual-ipv4-and-ipv6 default` in global configuration mode.
    - Reload the switch.
![[Pasted image 20250319232349.png]]

**Step 2: Configure the Dafault Gateway**
- The switch should be configured with a default gateway if it will be managed remotely from networks that are not directly connected.
- Note: If the switch receives its default gateway information from a router advertisement (RA) message, it does not require an IPv6 default gateway.
![[Pasted image 20250319232551.png]]

**Step 3: Verify Configuration**
- The `show ip interface brief` and `show ipv6 interface brief` commands help determine the status of physical and virtual interfaces.
- The output confirms that interface VLAN 99 is configured with both an IPv4 and IPv6 address.
- Note: An IP address applied to the SVI is for remote management access only and does not enable the switch to route Layer 3 packets.
![[Pasted image 20250319232707.png]]
