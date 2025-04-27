Fast Decisions with ASICs
- Switches use application-specific integrated circuits (ASICs) to make very fast Layer 2 forwarding decisions
- ASICs reduce frame-handling time and allow the switch to process more frame without slowing down

**Two Main Switching Methods**
- Store-and-Forwarding Switching (Cisco's primary method)
	- Switch waits and receive the entire frame
	- It performs a Cyclic Redundancy Check (CRC) to check for errors
	- Only error-free frames are forwarded
	- More reliable, but slightly slower
- Cut-Through Switching
	- Switch starts forwarding as soon as it reads the destination MAC address and knows where to send it
	- Does not wait for the whole frame
	- Faster, but errors may be forwarded because it doesn't check the full frame

![[Pasted image 20250427151518.png]]

[[Store-and-Forwarding]]
[[Cut-Through]]