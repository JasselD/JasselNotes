# Wireless Network Security
- What?
	- Wireless network security is crucial to protect the data transmitted over Wi-Fi networks from unauthorized access. Different Wi-Fi security protocols offer varying levels of encryption, authentication, and protection for data on a wireless network

# Wi-Fi Security Protocols
- WEP (Wired Equivalent Privacy):
	- What?
		- WEP is one of the earliest Wi-Fi security protocols and was designed to provide a level of security equivalent to what a wired network would have
		
		- It uses RC4 encryptoin to encrypt data, but WEP has several weaknesses, including short encryption keys and poor implementation, making it insecure by modern standards
		
	- Why avoid?
		- WEP is easilt cracked due to weak encryption and is considered obsolete. It is vulnerable to brute-force attacks and ket reuse attacks
		
	- When to use?
		- WEP should only be used in legacy systems where updating the security protocol is not an option
		
- WPA (Wi-Fi Protected Access):
	- What?
		- WPA was introduced as an improvement to WEP. It uses TKIP (Temporal Key Integrity Protocol) for encryption, which is more secure than WEP's RC4 encryption
		
	- Why use?
		- WPA improved security by addressing some of WEP's vulnerabilities, but it still has weaknesses. TKIP is more secure but has been outdated compared to newer encryption methods
		
	- When to use?
		- WPA is considered obsolete as it is not recommended for new network. It can still be found in older devices but should be replaced with WPA2 or WPA3 when possible
		
- WPA2 (Wi-Fi Protected Access 2):
	- What?
		- WPA2 uses AES (Advanced Encryption Standard) for encryption, which is much more secure than TKIP
		
		- WPA2 is widely used in modern Wi-Fi networks due to its strong security, offering both encryption and authentication
		
	- Why use?
		- Stronger than WPA and WEP because it uses AES encryption, which more resistant to attacks and offers better data protection
		
	- WPA2 Personal vs. WPA2 Enterprise:
		- WPA2 Personal:
			- Uses a standard passphrase for authentication, making it suitable for home networks or small business setups
			
		- WPA2 Enterprise:
			- Uses 802.1X authentication and RADIUS servers, making it more suitable for large networks with multiple users needing individual authentication
			
	- When?
		- WPA2 should be standard for most networks as it provides strong security with AES encryption
		
- WPA3 (Wi-Fi Protected Access 3):
	- What?
		- WPA3 is the latest Wi-Fi security standard, designed to provide even stronger encryption and protection against various attacks, such as bruto-force and offline dictionary attacks
		- WPA3 uses SAE (Simultaneous Authentication of Equals) instead of PSK (Pre-Shared Key), which enchances key exchange security
	- Why use?
		- WPA3 offers the highest level of security for modern wireless networks. It provides stronger encryption, individualized encryption keys, and improved protection against offline attacks
		- It also introduces forward secrecy, ensuring that if a device's encryption key is compromised, past communicationsc cannot be decrypted
	- When to use?
		- WPA3 is recommended for newer networks and devices as it provides is the best available protection for wireless communication

# Authentication Methods: Personal vs. Enterprise
- WPA2 Personal (PSK):
	- What?
		- PSK (Pre-Shared Key) is the simpler authentication method where all devices share the same Wi-Fi password
		- It is ideal for home networks and small businesses with a small number of devices
	- Limitations of PSK:
		- Security risks arise if the password is weak or compromised. It does not offer individualized authentication for users
- WPA2 Enterprise (802.1X Authentication):
	- What?
		- WPA2 Enterprise uses 802.1X authentication with a RADIUS server. Each user has their own unique credentials, making it much more secure than WPA2 Personal
		- It is suited for large networks where individual authentication is required
	- Benefits:
		- Per-user authentication and encryption
		- Easier to manage for large organizations as you can control access with user-specific credentials

## QNA
- **What is the main difference between WPA2 Personal and WPA2 Enterprise?**
    
    - **WPA2 Personal** uses a **shared passphrase** for authentication (PSK), while **WPA2 Enterprise** uses **802.1X** authentication with a **RADIUS server**, providing **individualized user authentication**.
        
- **Why should you avoid using WEP in modern networks?**
    
    - **WEP** is **insecure** because it uses **weak encryption** and is vulnerable to **easy decryption**. It can be **cracked** quickly with modern tools, leaving networks open to **attacks**.
        
- **What is WPA3, and how does it improve upon WPA2?**
    
    - **WPA3** is the latest Wi-Fi security protocol, offering **stronger encryption**, **protection against offline dictionary attacks**, and **forward secrecy** to improve overall network security.
        
- **What is the advantage of using WPA2 Enterprise with 802.1X over WPA2 Personal?**
    
    - **WPA2 Enterprise** with **802.1X** provides **individualized authentication** and **stronger security** by using **unique credentials** for each user, compared to WPA2 Personal’s shared key.
        
- **Which Wi-Fi security protocol is the most secure and recommended for modern networks?**
    
    - **WPA3** is the **most secure** and **recommended** Wi-Fi security protocol for modern networks, offering the **best encryption** and protection against attacks.