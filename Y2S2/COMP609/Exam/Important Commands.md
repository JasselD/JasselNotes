# Essential Commands
- ipconfig /all:
	- Display detailed IP configuration for all interfaces
	
- ipconfig /release:
	- Releases the current DHCP lease
	
- ipconfig /renew:
	- Requests a new DHCP lease
	
- ipconfig /flushdns:
	- Clears the DNS resolver cache
	
- ping:
	- Tests connectivity to a host
	
- tracert:
	- Traces the route packets take to a destination
	
- nslookup:
	- Queries DNS records for a domain
	
- netstat -a:
	- Displays all active connections and listening ports
	
- arp -a:
	- Displays the ARP table

# When to use them?
- No internet connection:
	- ipconfig
	- ping
	- tracert
- Website not resolving:
	- nslookup
	- ipconfig /flushdns
- Need new IP from DHCP:
	- ipconfig /release + ipconfig /renew
- Track open ports:
	- netstat -a

# MCQ
**1. You want to view all active TCP connections and listening ports on a system. Which command should you use?**

A. `ping`  
B. `tracert`  
C. `netstat -a`  
D. `arp -a`

✅ **Correct Answer: C. `netstat -a`**

> Displays all active connections and listening ports.

---

**2. What command do you use to check if your system can reach another host (like google.com)?**

A. `nslookup`  
B. `ping`  
C. `ipconfig /flushdns`  
D. `netstat -a`

✅ **Correct Answer: B. `ping`**

> Sends ICMP packets to test basic connectivity.

---

**3. Which command clears the local DNS resolver cache on a Windows machine?**

A. `ipconfig /release`  
B. `ipconfig /all`  
C. `ipconfig /renew`  
D. `ipconfig /flushdns`

✅ **Correct Answer: D. `ipconfig /flushdns`**

> Removes stored DNS entries and forces fresh resolution.

---

**4. You suspect a DNS server is not responding correctly. What command can you use to directly query DNS records for a domain?**

A. `ping`  
B. `netstat -a`  
C. `nslookup`  
D. `tracert`

✅ **Correct Answer: C. `nslookup`**

> Queries DNS servers for domain resolution details.

---

**5. Which pair of commands would you use to release and renew your system’s DHCP IP address?**

A. `ipconfig /flushdns` and `ping`  
B. `ipconfig /all` and `nslookup`  
C. `ipconfig /release` and `ipconfig /renew`  
D. `tracert` and `netstat -a`

✅ **Correct Answer: C. `ipconfig /release` and `ipconfig /renew`**

> Releases the current DHCP lease and requests a new one.

---

**6. You want to view the detailed IP configuration of all network interfaces. Which command do you use?**

A. `ipconfig /all`  
B. `arp -a`  
C. `tracert`  
D. `netstat -a`

✅ **Correct Answer: A. `ipconfig /all`**

> Shows full IP, DNS, and adapter info.

---

**7. Which command displays the ARP table showing IP-to-MAC address mappings?**

A. `tracert`  
B. `netstat -a`  
C. `arp -a`  
D. `ipconfig /flushdns`

✅ **Correct Answer: C. `arp -a`**

> Lists cached mappings of IP addresses to MAC addresses.

---

**8. What does the `tracert` command help diagnose?**

A. MAC address conflicts  
B. DNS misconfiguration  
C. Routing paths and delays between your PC and a remote host  
D. Open network ports

✅ **Correct Answer: C. Routing paths and delays between your PC and a remote host**

> It traces the route taken by packets and shows each hop.

---

**9. If you’re experiencing issues connecting to a website, which command would help verify whether it’s a DNS issue?**

A. `arp -a`  
B. `ipconfig /all`  
C. `nslookup`  
D. `tracert`

✅ **Correct Answer: C. `nslookup`**

> Helps determine whether the domain name is resolving correctly.

---

**10. A user complains they have no internet. Which set of commands is best to start troubleshooting with?**

A. `netstat -a`, `arp -a`  
B. `ipconfig /all`, `ping`, `tracert`  
C. `nslookup`, `ipconfig /flushdns`  
D. `ipconfig /release`, `netstat -a`

✅ **Correct Answer: B. `ipconfig /all`, `ping`, `tracert`**

> These commands help check local config, connectivity, and route tracing.