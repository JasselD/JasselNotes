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
