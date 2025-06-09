**SSH (Secure Shell)**
- What?
	- Network protocol that allows you to securely access network devices, such as routers and switches, from a remote location
	- It uses encryption to protect the data, including username and passwords, from being intercepted by unauthorized parties
- Why?
	- Security: 
		- SSH encrypts the entire communication session, which means your data is safe from eavesdropping
	- Remote Management:
		- You can manage devices remotely, saving time and allowing access without being physically near the device
	- Authentication:
		- Can be used either passwords or public/private key pairs for authentication
- How?
	- SSH keys: 
		- Uses public and private keys for a more secure authentication process. When a devices tries to access another device, the public ket encrypts the communication, and only the corresponding private key can decrypt it
	- Command
- How to Connect via SSH
	- Once SSH is configured on your device, you can connect from your computer using a terminal or SSH client like PuTTy

**Telnet**
- What?
	- Older remote access protocol that allows you to manage devices remotely. Unlike SSH, Telnet sends data in plaintext without any encryption, which makes it vulnerable to security risks
- Why?
	- Does not enc