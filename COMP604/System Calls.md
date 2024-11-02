- Programmatic way in which a computer program requests a service from the kernel of the OS
- These calls are generally available as routines written in C or C++
- Provide an interface to the services made available by an OS

User Mode 
- Does not have direct access to the memory and hardware
- If program crash while running in User Mode, not everything would crash

Kernel Mode (Privileged Mode)
- Have direct access to the memory and hardware
- If program crash while running in Kernel Mode, the whole thing will crash

Types of System Calls
- Process Control
  - end, abort
  - load, execute
  - create process, terminate process
  - get process attributes, set process attricutes
  - wait for time
  - wait event, signal event
  - allocate and free memory
- File Manipulation
- Device Management
- Information Management
- Communications
