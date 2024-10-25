- WPA and WPA2 are <mark style="background: #ABF7F7A6;">security protocols and security certification programs</mark> developed by the Wi-Fi Alliance to secure wireless networks
- Both were designed to <mark style="background: #ABF7F7A6;">address vulnerabilities</mark> found in earlier security protocol called WEP

**WPA (Wi-Fi protected access)
- Features:
	- <mark style="background: #ABF7F7A6;">TKIP (Temporal Key Integrity Protocol)</mark>
		- Used for <mark style="background: #ABF7F7A6;">encryption</mark>
		- Dynamically <mark style="background: #ABF7F7A6;">changes the keys</mark> used to encrypt every packet
		- Adds a per-packet key mixing function, a message integrity check, and other measures to prevent replay attacks
	- <mark style="background: #ABF7F7A6;">PSK (Pre-shared key)</mark>
		- Used for <mark style="background: #ABF7F7A6;">authentication</mark>
		- WPA-Personal (PSK): For <mark style="background: #ABF7F7A6;">home use</mark>, a shared passphrase is used for authentication
		- WPA-Enterprise: In corporate environments, use a <mark style="background: #ABF7F7A6;">Radius server</mark> for centralized authentication <mark style="background: #ABF7F7A6;">(802.1X authentication)</mark>
	- Security level:
		- TKIP: medium
		- PSK: low-medium (depends on passphrase)
		- 802.1x: high

**WPA2 
- Features:
	- AES-CCMP
		- AES
			- Used for encryption
			- Block cipher encryption algorithm (128-bit blocks)
			- Supports key sizes of 128, 192, and 256 bits
			- Strong, secure, widely used encryption
		- CCMP
			- Mode of operation for AES in WPA2
			- Combines:
				- Counter Mode (CTR): Encrypts data using unique counters per packet
				- CBC-MAC: Ensures data integrity/authentication
	- PSK (Pre-shared key)
		- Used for authentication
		- WPA2-Personal (PSK): For home use with shared passphrase
		- WPA2-Enterprise: Suitable for corporate environments using 802.1X authentication via a Radius server for more secure and dynamic key generation
	- Security level:
		- PSK: Medium
		- AES-CCMP: High
		- 802.1x: High

**WPA vs WPA2
![[Pasted image 20241026004625.png]]
