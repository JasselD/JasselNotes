Collisions vs Congestion
- Collision:
	- Happens when two or more devices try to send data at the same time on the same network segment
- Congestion
	- Too much data traffic on the network, like traffic jams

Collision Domains
- Legacy Hub-Based Networks:
	- Devices share the same bandwidth:
		- All devices are in one large collision domain
- Switches:
	- Break up collision domains:
		- Each port on a switch is its own collision domain (if operating in half-duplex)

Duplex Modes
- Half-Duplex:
	- Devices can send or receive, but not at the same time
	- Collision domains exist when switch ports are operating in half-duplex
- Full-Duplex:
	- Devices can send and receive at the same time
	- No collisions occur in full-duplex mo