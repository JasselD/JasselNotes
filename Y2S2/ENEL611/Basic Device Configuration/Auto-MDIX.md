- **Auto-MDIX and Cable Types**
    
    - Previously, specific cable types (**straight-through** or **crossover**) were required for different device connections
        
    - **Switch-to-switch** or **switch-to-router** connections needed different Ethernet cables
    
- **Auto-MDIX Feature**
    
    - Automatically detects and configures the required cable type
        
    - Eliminates the need for manually selecting straight-through or crossover cables
        
    - On older switches **without auto-MDIX**, cable selection still matters:
        
        - **Straight-through** for servers, workstations, or routers
            
        - **Crossover** for switches or repeaters
        
- **Enabling Auto-MDIX**
    
    - Newer Cisco switches use the `mdix auto` interface configuration mode command
        
    - Speed and duplex settings must be set to **auto** for auto-MDIX to function properly

 [[Verify Switch Port Configuration]]
 