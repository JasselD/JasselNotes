**Processor Modes**
- Kernel (Supervisor mode)
	 Executing code has unrestricted access to hardware
	 
- User Mode
	 Executing code has no direct access to hardware and memory beyond its own process

**Interrupts**
- Handling of interrupts are transparent to the user program
- On Return from interrupts, OS restores the state of user program
- Continues at exactly the same point as when it was interrupted

**Exceptions**
- Does the User Program has exception handling ?
	 YES : OS adjust user program state and calls its handler
	 NO : OS kill the user program
	 
- Effects of exceptions are visible to user programs
- Causes abnormal execution flow

**System Call**
- User program executes a [[trap instruction]] (system call)
- Processor hardware calls the OS
- OS identifies the required service and parameters and executes it
- Result of the call is return through a register
- Execution returns to user programs (rfi)

![[Screenshot 2024-07-28 at 9.34.08 PM.png]]

![[Screenshot 2024-07-28 at 9.34.51 PM.png]]