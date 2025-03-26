**Input Errors**
- Total number of errors. Includes runts, giants, no buffer, CRC, frame, overrun, and ignored counts
- **<mark style="background: #ABF7F7A6;">Runts (Undersized Frames)</mark>**
    
    - Ethernet frames **smaller than 64 bytes** (minimum valid size)
        
    - Often caused by **collisions** in half-duplex networks
        
    - Indicate possible **network congestion or duplex mismatches**
        
- **<mark style="background: #ABF7F7A6;">Causes of Runts</mark>**
    
    - **Half-duplex collisions**
        
    - **Faulty network cables** or poor connections
        
    - **Mismatched speed or duplex settings** between devices
        
- **<mark style="background: #ABF7F7A6;">Troubleshooting Runts</mark>**
    
    - Check and **match duplex settings** on both ends of the connection
        
    - Ensure proper **cabling and connections**
        
    - Monitor **network traffic and congestion**
        
    - Use `show interfaces` on Cisco devices to check for runt counters


- **<mark style="background: #ABF7F7A6;">Giants (Oversized Frames)</mark>**
    
    - Ethernet frames **larger than the maximum allowed size** (typically **1518 bytes** for standard Ethernet, **1522 bytes** with VLAN tagging)
        
    - Can be caused by **misconfigured MTU (Maximum Transmission Unit) settings**
        
- **Causes of Giants**
    
    - **Jumbo frames** sent on a network that doesn’t support them
        
    - **MTU mismatches** between devices
        
    - **Malfunctioning network hardware** (e.g., faulty NICs or switches)
        
- **Troubleshooting Giants**
    
    - Check and **standardize MTU settings** across devices
        
    - Ensure **jumbo frames** are supported if enabled
        
    - Monitor network interfaces using `show interfaces` on Cisco devices to check for giant counters

- **<mark style="background: #ABF7F7A6;">Cyclic Redundancy Check (CRC) Errors</mark>**
    
    - Occur when a received Ethernet frame **fails the CRC check**, indicating data corruption
        
    - Found using `show interfaces` on Cisco devices
        
- **Causes of CRC Errors**
    
    - **Network interference** (e.g., electromagnetic interference from nearby devices)
        
    - **Faulty cables or connectors** (damaged or poor-quality cables)
        
    - **Mismatched duplex settings**, leading to late collisions
        
    - **High network congestion** causing frame corruption
        
    - **Hardware issues** (e.g., failing network interface cards or switch ports)
        
- **Troubleshooting CRC Errors**
    
    - Replace or check **cables and connectors** for damage
        
    - Verify **duplex and speed settings** on both ends of the connection
        
    - Reduce **electromagnetic interference** by repositioning network cables
        
    - Monitor network congestion and **optimize traffic flow**

- **<mark style="background: #ABF7F7A6;">Output Errors</mark>**
    
    - Indicate issues when transmitting frames from an interface
        
    - Found using the `show interfaces` command on Cisco devices
        
    - Total **output errors** include **collisions, buffer overflows, and interface congestion**
        
- **Causes of Output Errors**
    
    - **High network traffic** causing interface congestion
        
    - **Duplex mismatches**, leading to collisions and retransmissions
        
    - **Faulty cables or connectors**
        
    - **Overloaded switch or router interface buffers**
        
    - **Hardware failures** (e.g., bad network interface cards or switch ports)
        
- **Troubleshooting Output Errors**
    
    - Check and **match duplex settings** on both ends of the connection
        
    - Monitor **interface utilization** and consider **load balancing or upgrading bandwidth**
        
    - Replace **damaged cables or faulty hardware**
        
    - Reduce excessive broadcast or multicast traffic in the network

- **<mark style="background: #ABF7F7A6;">Collisions</mark>**
    
    - Occur when two devices on a network try to send data at the same time, causing their signals to interfere with each other
        
    - Common in **half-duplex** networks (e.g., older hubs)
        
    - Results in **data loss**, and devices must resend the data
        
- **Causes of Collisions**
    
    - **Half-duplex communication**, where devices can’t send and receive simultaneously
        
    - **Network congestion** or high traffic causing frequent data transmissions
        
    - **Faulty or misconfigured network hardware**
        
    - **Incorrect duplex settings** (e.g., one device in full-duplex and the other in half-duplex)
        
- **Impact of Collisions**
    
    - Decreased network **performance** due to retransmissions
        
    - **Increased network delays**
        
    - **Potential for network congestion** in busy environments
        
- **Troubleshooting Collisions**
    
    - Ensure devices are set to **full-duplex** if possible (eliminates collisions)
        
    - **Match duplex settings** on both ends of the connection
        
    - Check for **network congestion** and upgrade equipment if necessary
        
    - Replace **old hubs** with **modern switches** to eliminate collision domains

- **<mark style="background: #ABF7F7A6;">Late Collisions</mark>**
    
    - Occur when a collision is detected **after the 512-bit time window** (the time it takes for a signal to travel across the network)
        
    - Typically indicate problems with **network configuration or hardware issues**
        
- **Causes of Late Collisions**
    
    - **Duplex mismatches** between devices (e.g., one side set to full-duplex, the other to half-duplex)
        
    - **Excessive network congestion** leading to delayed packet transmission
        
    - **Faulty cables or connectors** causing signal degradation
        
    - **Distance issues** in a network, such as too-long cable runs exceeding the maximum allowed distance
        
    - **Improperly configured network equipment**, like switches or NICs
        
- **Impact of Late Collisions**
    
    - **Increased latency** and **reduced network performance**
        
    - **Data corruption** due to collisions occurring after the transmission has started
        
    - **Frequent retransmissions** leading to network congestion
        
- **Troubleshooting Late Collisions**
    
    - Ensure devices are set to the **same duplex mode** (full-duplex or half-duplex)
        
    - **Check cable quality** and **replace faulty cables**
        
    - Verify that **network equipment is properly configured**
        
    - Check for **excessive network traffic** and ensure the network infrastructure can handle the load