- <mark style="background: #ABF7F7A6;">Redundant Array of Independetn Disks</mark> (RAID)
- A technology that combines multiple physical hard drives into one unit for redundancy or performance
- Types:
	- RAID 0 <mark style="background: #ABF7F7A6;">(Striping)</mark>
		- Data is <mark style="background: #ABF7F7A6;">split evenly across two or more disks</mark> to <mark style="background: #ABF7F7A6;">improve performance</mark>
		- Pros: Increased read/write speeds
		- Cons: <mark style="background: #ABF7F7A6;">No redundancy</mark>. If <mark style="background: #ABF7F7A6;">one disk fails</mark>, <mark style="background: #ABF7F7A6;">all data is lost</mark>. <mark style="background: #ABF7F7A6;">No fault tolerance</mark>
	- RAID 1 <mark style="background: #ABF7F7A6;">(Mirroring)</mark>
		- Data is <mark style="background: #ABF7F7A6;">duplicated on two or more disks</mark>, so each disk holds the same data
		- Pros: Redundancy; if one disk fails, the other still has the data
		- Cons: Reduced storage effieciency (need twice the storage). <mark style="background: #ABF7F7A6;">Slower write speeds</mark>
	- RAID 5 (Striping with Parity)
		- Data is split across three or more disks, with parity information distributed across all disks. Parity allows recovery if a disk fails
		- Pros: Redundancy and good storage effiency
		- Cons: Slower write speeds due to parity calculations. Recovery can take time
	- RAID 0+1 (Striped Mirrors)
		- Combines RAID 0 and RAID 1. Data is striped (like RAID 0) for speed and mirrored (like RAID 1) for redundancy
		- Pros: Combines the benefits of RAID 0 and RAID 1 (speed and redundancy)
		- Cons: Requires more disk (minimum 4). No fault tolerance for mirror set failure

![[Pasted image 20241026232001.png]]

**Striped
- Spread

**Parity
- Information that is used to r