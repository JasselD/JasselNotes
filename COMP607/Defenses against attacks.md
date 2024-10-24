**Layering (Defense in Depth)
- Defense: <mark style="background: #ABF7F7A6;">Implemet multiple, independent layers of security</mark> to protect your system. This way, even <mark style="background: #ABF7F7A6;">if one layer fails others can remain intact to defend</mark>
- **Examples:**
	- **Firewalls:** Use both <mark style="background: #ABF7F7A6;">external and internal firewalls</mark> to monitor and filter traffic.
	- **Encryption:** <mark style="background: #ABF7F7A6;">Protect data at rest</mark> and in transit with encryption to add an extra layer of security.
	- **Intrusion Detection Systems (<mark style="background: #ABF7F7A6;">IDS</mark>):** <mark style="background: #ABF7F7A6;">Monitor for suspicious activity</mark> across different points of your network.
	- **Physical Security:** <mark style="background: #ABF7F7A6;">Use badges, locks, and biometric scanners</mark> to protect access to critical facilities.

**Limiting (Access Control)
- Defence: <mark style="background: #ABF7F7A6;">Restrict access to systems, files, and data</mark> to only those individual or processes that require it. This <mark style="background: #ABF7F7A6;">limits the attack surface</mark>
- **Examples:**
	- **Role-based Access Control (<mark style="background: #ABF7F7A6;">RBAC</mark>):** <mark style="background: #ABF7F7A6;">Assign roles with specific permissions</mark>, ensuring that users can only access the information they need.
	- **Principle of Least Privilege (<mark style="background: #ABF7F7A6;">PoLP</mark>):** <mark style="background: #ABF7F7A6;">Only give users and applications the minimum level of access required</mark> to perform their tasks.
	- **Network Segmentation:** <mark style="background: #ABF7F7A6;">Limit communication between different parts of the network</mark>, isolating sensitive data.
	- **Strong Authentication:** <mark style="background: #ABF7F7A6;">Implement multi-factor authentication (MFA)</mark> to ensure that only authorized users gain access.

**Diversity (Varied Security Controls)
- Defense: Use <mark style="background: #ABF7F7A6;">diverse technologies and methods</mark> to protects your systems, <mark style="background: #ABF7F7A6;">reducing the risk of a single-point failure</mark>
- **Examples:**
	- **Different Firewalls and Antivirus Vendors:** Use firewalls and security tools from different vendors to prevent vulnerabilities from affecting all layers.
	- **Multiple Authentication Methods:** Combine biometrics, password-based logins, and token-based authentication for stronger protection.
	- **Varied Operating Systems:** In critical systems, use different OSes for different servers or components to reduce the risk of a widespread attack exploiting the same vulnerability.

**Obscurity (Hiding Details)
- Defense: Keep system details hidden to make it harder for attackers to understand how to exploit them
- **Examples:**
	- **Non-standard Port Usage:** Use non-default ports for critical services (e.g., SSH or Remote Desktop) to make them harder to detect.
	- **Code Obfuscation:** For web apps, obfuscate sensitive code so that attackers can't easily reverse-engineer it.
	- **Masking Network Topology:** Avoid revealing your internal network structure, IP addresses, or configurations to external parties or public documentation.
	- **Honeypots:** Deploy decoy systems that appear valuable but are designed to trap and analyze attackers, diverting them away from real assets.

**Simplicity (Ease of Management and Security)
- Defense: Keep security mechanisms simple and manageble to avoid introducing unnecessary complexity, which often leads to vulnerabilities
- **Examples:**
	- **Unified Security Policies:** Create clear, enforceable policies that apply uniformly across the organization, making them easy to follow and audit.
	- **Automated Patch Management:** Simplify the process of keeping software up to date with automated patching tools, reducing the chance of missed updates.
	- **Simplified Network Architecture:** Avoid overly complex network designs to make it easier to monitor and secure traffic.
	- **Streamlined Access Controls:** Use centralized identity and access management (IAM) systems to keep access controls consistent across the organization.


