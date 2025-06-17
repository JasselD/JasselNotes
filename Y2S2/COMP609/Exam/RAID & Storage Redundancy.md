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
- Disk Redundancy:
	- Using RAID to reduce risk of disk failure
	
- Data Backups:
	- Copying data to external or cloud systems

# Data Backup Strategies
- Full Backup:
	- Copies everything
	
- Incremental:
	- Copies changes since last backup
	
- Differential:
	- Copies changes since last full backup
[[Backup Types]]

- Cloud backup offers scalability & remote access

# Short QNA
- **What does RAID stand for?**  
    RAID stands for **Redundant Array of Independent Disks**.
    
- **What are the three main benefits of using RAID?**  
    RAID improves **performance**, **redundancy**, and **availability** of data storage.
    
- **Which RAID level provides high speed but no fault tolerance?**  
    **RAID 0** provides high speed but has **no fault tolerance**.
    
- **Which RAID level mirrors data to provide redundancy?**  
    **RAID 1** uses **mirroring** to create a 1:1 copy of data for redundancy.
    
- **How many disk failures can RAID 5 tolerate?**  
    **RAID 5** can tolerate the **failure of one disk** without data loss.
    
- **What is RAID 0+1?**  
    **RAID 0+1** is a combination of **striping and mirroring**, also called a **mirrored stripe set**, offering both speed and redundancy.
    
- **What is disk redundancy?**  
    Disk redundancy refers to the use of technologies like **RAID** to ensure that data is not lost if a disk fails.
    
- **What is the difference between a full backup and an incremental backup?**  
    A **full backup** copies **all data**, while an **incremental backup** only copies data that has **changed since the last backup**.
    
- **What does a differential backup do?**  
    A **differential backup** copies all data that has changed **since the last full backup**.
    
- **What is an advantage of cloud backup?**  
    **Cloud backup** offers **scalability** and **remote access** to data from anywhere.

# Long QNA
- **Explain what RAID is and how it benefits data storage systems.**  
    RAID, or **Redundant Array of Independent Disks**, is a storage technology that combines multiple physical hard drives into a single logical unit. It enhances system **performance** by allowing faster data access, provides **redundancy** to protect against disk failure, and improves **availability** by minimizing downtime. Different RAID levels offer varying balances between speed, data protection, and storage efficiency, depending on the system's needs.
    
- **Compare and contrast RAID 0, RAID 1, and RAID 5.**
    
    - **RAID 0 (Striping):** This level splits data evenly across multiple disks to maximize speed. However, it offers **no fault tolerance**—if one disk fails, all data is lost.
        
    - **RAID 1 (Mirroring):** This level creates an exact copy of data on two or more disks, providing high **fault tolerance** but requiring double the storage space.
        
    - **RAID 5 (Striping with Parity):** This level balances **speed and redundancy** by distributing data and parity information across three or more disks. It can survive the failure of one disk without data loss.
        
- **What is RAID 0+1, and in what situations would it be used?**  
    RAID 0+1 is a hybrid RAID configuration that combines **striping (RAID 0)** for performance and **mirroring (RAID 1)** for redundancy. It creates mirrored sets of striped arrays, providing both **high speed** and **fault tolerance**. It is commonly used in **high-performance environments** like enterprise applications, where both data speed and safety are critical.
    
- **Describe three different types of data backup strategies and their advantages.**
    
    - A **full backup** creates a complete copy of all data. It is simple and comprehensive but takes the most time and storage.
        
    - An **incremental backup** saves only the data that has changed since the last backup (whether full or incremental). It is fast and uses less storage but can be slower to restore.
        
    - A **differential backup** saves all data changed since the last full backup. It offers a middle ground in restore speed and backup size.  
        Together, these strategies allow organizations to tailor their **data protection** approach based on time, storage, and recovery needs.
        
- **Why is it important to have both RAID and regular data backups in place?**  
    While RAID protects against **disk failures**, it does **not guard against data corruption, accidental deletion, ransomware, or site disasters**. Therefore, combining **RAID** for hardware-level protection with **regular backups** ensures **comprehensive data protection**. Backups provide a recoverable version of the data even if the RAID system becomes compromised or the entire system is lost.