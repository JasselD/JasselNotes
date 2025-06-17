# RAID
- What?
	- RAID is a technology that combines multiple physical hard drives into one logical unit to improve:
		- Performance
		- Redundancy (data protection)
		- Availability
	- Different RAID levels offer different balances of performance, reliability, and storage efficiency

# Common Raid Levels
- RAID 0:
	- Name:
		- Stripping
	- Features:
		- High speed (no redundancy)
	- Fault Tolerance:
		- None
	- Use Case:
		- Video editing, temp storage
		
- RAID 1:
	- Name:
		- Mirroring
	- Features:
		- 1:1 copy of data (mirror)
	- Fault Tolerance:
		- Yes (1 disk failure)
	- Use Case:
		- Critical data backup
		
- RAID 5:
	- Name:
		- Stripping with Parity
	- Features:
		- Combines speed and redundancy
	- Fault Tolerance:
		- Can tolerate 1 disk failure
	- Use Case:
		- Databases, file servers
		
- - RAID 0+1:
	- Name:
		- Mirrored Stripe Set
	- Features:
		- High speed and redundancy
	- Fault Tolerance:
		- 1 disk per mirror
	- Use Case:
		- High performance systems
[[RAID]]

# Storage Redundancy Methods
- Disk Redundanc