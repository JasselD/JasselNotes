**Input Errors**
- Total number of errors. Includes runts, giants, no buffer, CRC, frame, overrun, and ignored counts
- **Runts (Undersized Frames)**
    
    - Ethernet frames **smaller than 64 bytes** (minimum valid size)
        
    - Often caused by **collisions** in half-duplex networks
        
    - Indicate possible **network congestion or duplex mismatches**
        
- **Causes of Runts**
    
    - **Half-duplex collisions**
        
    - **Faulty network cables** or poor connections
        
    - **Mismatched speed or duplex settings** between devices
        
- **Troubleshooting Runts**
    
    - Check and **match duplex settings** on both ends of the connection
        
    - Ensure proper **cabling and connections**
        
    - Monitor **network traffic and congestion**
        
    - Use `show interfaces` on Cisco devices to check for runt counters


- **Giants (Oversized Frames)**
    
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