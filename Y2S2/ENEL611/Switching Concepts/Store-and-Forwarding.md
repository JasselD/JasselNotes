This is a more in-depth explaination

Error Checking
- Entire frame is received at the ingress port first
- The switch compares the Frame Check Sequence (FCS) at the end of the frame with its own FCS calculation
- If FCS matches -> Frame is error-free -> Frame is forwarded
- If FCS does not match -> Frame is dropped (not forwarded)
- FCS helps ensure the frame has no physical or data-link errors

Automatic Buffering
- Incoming frame is stored (buffered) before forwarding
- Supports different Ethernet speeds between ports
	- Example: Receiving from 100 Mbps port and sending to a 1 Gbps port
- Process:
	- Frame is stored in ingress buffer -> FCS is verified -> Frame moves to engress buffer -> Sent out