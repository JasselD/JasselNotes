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

**Step 2: Configure the