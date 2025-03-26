![[Pasted image 20250326163310.png]]

- **If the Interface is Down**
    
    - **Check cables**: Ensure the correct cables are used and check for any damage in the cables or connectors. Replace if faulty.
        
    - **Speed mismatch**: Verify that the speed settings are consistent on both ends of the connection. Speed is usually autonegotiated, but mismatches due to misconfiguration or hardware issues may cause the interface to go down. Set the same speed manually on both ends if necessary.
        
- **If the Interface is Up, but Connectivity Issues Persist**
    
    - **Check for excessive noise**:
        
        - Use the `show interfaces` command to check for increased counters of runts, giants, and CRC errors, which may indicate noise issues.
            
        - Find and remove the noise source if possible.
            
        - Ensure the cable does not exceed the maximum allowed length and that the correct type of cable is used.
            
    - **Check for excessive collisions**:
        
        - Verify if there are collisions or late collisions.
            
        - Check the **duplex settings** on both ends of the connection (as duplex is often autonegotiated).
            
        - If a duplex mismatch is detected, manually set the duplex to full-duplex on both ends.
            

