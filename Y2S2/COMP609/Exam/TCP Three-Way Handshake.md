# TCP Three-Way Handshake
- What?
	- Process used to establish a reliable connection between a client and server in a TCP/IP network. This handshake ensures synchronization between sender and receiver before actual data is transmitted

# Steps (SYN-SYN/ACK-ACK)
- SYN
	- The clients initiates the connection with a SYN (synchronize) message
	- Who sends it?:
		- Client
	- Purpose:
		- "Hey, I want to start a connection"
- SYN-ACK
	- The server replies with SYN-ACK (synchronize + acknowledgement)
	- Who sends it?:
		- Server
	- Purpose:
		- "Okay, Let's talk"
- ACK
	- The clients sends an ACK (acknowledgement) to finalize the connection
	- Who sends it?:
		- Client
	- Purpose:
		- "Confirmed. Ready to go"

# Key Concepts
- TCP is connection-oriented (not like UDP)
- Sequence numbers are initialized during this handshake
- The handshake is used before any real data transmission begins
- Ensures reliability and ordered delivery

# Short QNA
1. **What does TCP stand for?**  
    **Answer:** Transmission Control Protocol
    
2. **What is the purpose of the TCP three-way handshake?**  
    **Answer:** To establish a reliable connection between a client and server before data transmission.
    
3. **What are the three steps in a TCP handshake?**  
    **Answer:** SYN, SYN-ACK, ACK
    
4. **Who sends the initial SYN message?**  
    **Answer:** The client
    
5. **What does the server send in response to a SYN message?**  
    **Answer:** SYN-ACK
    
6. **What does the client send to complete the handshake?**  
    **Answer:** ACK
    
7. **What is established during the TCP handshake to ensure reliable delivery?**  
    **Answer:** Sequence numbers
    
8. **Is TCP connection-oriented or connectionless?**  
    **Answer:** Connection-oriented
    
9. **Is data transmitted during the handshake?**  
    **Answer:** No, real data is transmitted only after the handshake is complete.

# Long QNA
- **Explain the TCP three-way handshake process and its purpose.**  
    **Answer:**  
    The TCP three-way handshake is a method used to establish a reliable connection between a client and a server. It involves the following steps:
    
    - **SYN (synchronize):** The client initiates the connection by sending a SYN message to the server to indicate it wants to start communication.
        
    - **SYN-ACK (synchronize-acknowledgment):** The server responds with a SYN-ACK message to acknowledge the client's request and signal readiness.
        
    - **ACK (acknowledgment):** The client replies with an ACK message to confirm the connection setup.
        
    
    This process ensures both parties are synchronized and ready for reliable data transfer. It also initializes sequence numbers for ordered data delivery and prevents data loss or duplication.
    
- **How does the TCP handshake differ from protocols like UDP, and why is it important?**  
    **Answer:**  
    Unlike UDP, which is **connectionless**, TCP uses a **connection-oriented** approach via the three-way handshake. This is important because it:
    
    - **Ensures reliability**: Both sender and receiver confirm readiness.
        
    - **Establishes sequence numbers**: Critical for keeping data in order and handling retransmissions.
        
    - **Prevents data loss**: No data is transmitted until the connection is successfully established.
        
    
    UDP, by contrast, sends data without verifying whether the receiver is ready, which is faster but less reliable.