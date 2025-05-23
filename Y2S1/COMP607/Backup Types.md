- <mark style="background: #ABF7F7A6;">Fault tolerance</mark> is the <mark style="background: #ABF7F7A6;">prevention of data loss</mark> if a <mark style="background: #ABF7F7A6;">component fails</mark>
**Types:
- Full Backup:
	- <mark style="background: #ABF7F7A6;">Complete copy of all data</mark> is made
	- Pros: Simple to restore
	- Cons: Time-consuming and requires a lot of storage
- Diffrential Backup: 
	- Backs up all the <mark style="background: #ABF7F7A6;">data that has changed since the last full backup</mark>
	- Pros: Faster than full backup, but <mark style="background: #ABF7F7A6;">slower than incremental</mark>. Easier to restore than incremental backups because you only need the last full backup and the most recent differential backup
	- Cons: Size grows over time, as each differential backup includes changes from the last full backup onward
- Incremental Backup:
	- Backs up only the <mark style="background: #ABF7F7A6;">data that has changed since the last backup</mark> (whether full or incremental)
	- Pros: Fastest and uses the least storage space
	- Cons: Slower to restore because you need <mark style="background: #ABF7F7A6;">multiple sets of backup files</mark>
- Copy Backup
	- A backup that is <mark style="background: #ABF7F7A6;">almost the same as full backup</mark> but <mark style="background: #ABF7F7A6;">does not interfere with your scheduled backups</mark>
	- Pros: Useful for <mark style="background: #ABF7F7A6;">ad hoc backups</mark>, like when <mark style="background: #ABF7F7A6;">performing system maintanance</mark>
	- Cons: Not part of your regular backup plan, so it may cause confusion if not managed properly
- Gratherfather-father-son Backup <mark style="background: #ABF7F7A6;">(GFS)</mark>
	- <mark style="background: #ABF7F7A6;">Rotation scheme</mark> used to manage and organize backups over time, ensuring <mark style="background: #ABF7F7A6;">multiple restore points</mark> while optimizing storage space
	- <mark style="background: #ABF7F7A6;">Son (Daily backup)</mark>
	- <mark style="background: #ABF7F7A6;">Father (Weekly backup)</mark>
	- <mark style="background: #ABF7F7A6;">Grandfather (Monthly backup)</mark>
	- Pros:
		- Multiple restore points
		- Efficient storage use
		- Easy organisation
	- Cons
		- Complexity
		- Storage (need significant size)
		- Retention gaps

![[Pasted image 20241026230205.png]]
