![[Pasted image 20250319231210.png]]
1. SYST
	- **System LED**
	    The LED shows the system's power and status. If it's off, the system is not powered on. A green LED means the system is functioning normally, while an amber LED indicates the system is powered but not operating properly.
2. RPS
	- **Redundant Power System (RPS) LED**
		The RPS LED shows the status of the RPS. If the LED is off, the RPS is either off or not properly connected. A green LED indicates that the RPS is connected and ready to provide backup power. If the LED blinks green, the RPS is connected but unavailable because it is powering another device. An amber LED means the RPS is in standby mode or experiencing a fault. If the LED blinks amber, it indicates that the internal power supply in the switch has failed, and the RPS is supplying power.
3. STAT
	- **Port Status LED**
		The port status mode is indicated by the LED color. When the LED is off, there is no link, or the port is administratively shut down. A green LED indicates a link is present, while a blinking green LED shows activity with data being sent or received. An alternating green-amber LED signals a link fault. An amber LED means the port is blocked to prevent a loop in the forwarding domain and is not forwarding data. If the LED is blinking amber, the port is blocked to prevent a possible loop in the forwarding domain.
4. DUPLX
	- **Port Duplex LED**
		Indicates that the port duplex mode is selected when the LED is green. When selected, port LEDs that are off are in half-duplex mode. If the port LED is green, the port is in full-duplex mode.
5. SPEED
	- **Port Speed LED**
		Indicates that the port speed mode is selected. When selected, the port LEDs will display colors with different meanings. If the LED is off, the port is operating at 10 Mbps. If the LED is green, the port is operating at 100 Mbps. If the LED is blinking green, the port is operating at 1000 Mbps.
6. PoE
	- **Power over Ethernet (PoE) Mode LED**
		If PoE is supported, the PoE mode LED shows the status. If the LED is off, PoE mode is not selected, and no ports are denied power or in a fault condition. A blinking amber LED means PoE mode is not selected, but at least one port has been denied power or has a PoE fault. A green LED indicates PoE mode is selected, and the port LEDs show different statuses. If a port LED is off, PoE is off; if it's green, PoE is on. An alternating green-amber LED means PoE is denied because the switch's power capacity would be exceeded. A blinking amber LED indicates a PoE fault, and an amber LED means PoE for the port has been disabled.