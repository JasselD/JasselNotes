**SSH (Secure Shell)**
- What?
	- <mark style="background: #ABF7F7A6;">Network protocol</mark> that allows you to <mark style="background: #ABF7F7A6;">securely access network devices</mark>, such as <mark style="background: #ABF7F7A6;">routers and switches</mark>, from a <mark style="background: #ABF7F7A6;">remote location</mark>
	- It uses <mark style="background: #ABF7F7A6;">encryption</mark> to protect the data, including <mark style="background: #ABF7F7A6;">username and passwords</mark>, from being intercepted by unauthorized parties
- Why?
	- Security: 
		- SSH <mark style="background: #ABF7F7A6;">encrypts the entire communication session</mark>, which means your data is safe from <mark style="background: #ABF7F7A6;">eavesdropping</mark>
	- Remote Management:
		- You can <mark style="background: #ABF7F7A6;">manage devices remotely</mark>, saving time and allowing access without being physically near the device
	- Authentication:
		- Can be used either <mark style="background: #ABF7F7A6;">passwords or public/private key pairs</mark> for authentication
- How?
	- SSH keys: 
		- Uses <mark style="background: #ABF7F7A6;">public and private keys</mark> for a more secure authentication process. When a devices tries to access another device, the <mark style="background: #ABF7F7A6;">public key encrypts the communication</mark>, and <mark style="background: #ABF7F7A6;">only the corresponding private key</mark> can decrypt it
	- Command
- How to Connect via SSH
	- Once SSH is configured on your device, you can connect from your computer using a terminal or SSH client like PuTTy

**Telnet**
- What?
	- <mark style="background: #ABF7F7A6;">Older remote access protocol</mark> that allows you to manage devices remotely. Unlike SSH, Telnet <mark style="background: #ABF7F7A6;">sends data in plaintext without any encryption</mark>, which makes it <mark style="background: #ABF7F7A6;">vulnerable</mark> to security risks
- Why?
	- <mark style="background: #ABF7F7A6;">Does not encrypt data</mark>, so sensitive information like passwords can be intercepted by attackers who can access the network
	- Should be <mark style="background: #ABF7F7A6;">used in trusted environments</mark> or with devices that do not support SSH
- How?
	- It operates over port 23 and allows for basic remote access without encryption

**<mark style="background: #ABF7F7A6;">QNA</mark>
- What is the difference between SSH and Telnet?
	- **SSH** is a **secure, encrypted** protocol for remote access, while **Telnet** is an older **unsecure** protocol that transmits data in **plaintext**, making it vulnerable to eavesdropping.
	
- Why should you prefer SSH over Telnet for remote access?
	- **SSH** should be preferred because it provides **encryption** for secure communication, preventing **data interception**, including sensitive information like **passwords**, while **Telnet** sends data without encryption, exposing it to security risks.
	
- Which encyption method does SSH uses to secure communication?
	- **SSH** uses **public/private key encryption** to secure the communication between devices. The **public key** encrypts the data, and the **private key** decrypts it, ensuring secure communication.
	
- What is the default port used by Telnet for remote access?
	- **Telnet** uses **port 23** by default for remote access to network devices.