This is a more in-depth explaination

Error Checking
- Entire frame is received at the ingress port first
- The switch compares the Frame Check Sequence (FCS) at the end of the frame with its own FCS calculation
- If FCS matches -> Frame is error-free -> Frame is forwarded
- If FCS does not match -> Frame is dropped (not forwarded)
- FCS helps ensure the frame has no physical or data-l9ink 