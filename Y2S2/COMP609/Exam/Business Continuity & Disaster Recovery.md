# Business Continuity
- What?
	- Business Continuity is an organization's ability to maintain essential operations during and after a disruptive event such as:
		- Hurricanes
		- Earthquakes
		- Fires
		- Cyberattacks
	- Business Continuity Plan provides strategies, procedures, and resources needed to ensure ongoing business operations during disruption

# BCP Planning & Testing Steps
1. Identify threats and exposure
2. Create prevention and recovery procedures
3. Test and evaluate the plan
4. Train employees
5. Update regularly

# Succesion Planning
- Pre-defines who takes over if a key person is:
	- Unavailable
	- Incapacitated
	- Deceased
- This ensures continuity in leadership and critical decision-making

# Business Impact Analysis (BIA)
- Identifies critical business functions
- Assesses the impact of their loss
- Uses risk assessments to find potential threats
- Helps to prioritize recovery plans based on operational importance

# Data Storage and Redundancy & Backup
- What?
	- Copying importatn information to another medium or offsite location for disaster recovery purposes

# Backup Strategy: 5 W's
1. What should be backed up?
2. When should backups occur?
3. Where should backups be stored?
4. Which media will be used?
5. Who/what tool performs the backup?

# Backup Methods
- Full backup
	- Backs up all selected files
- Incremental:
	- Backs up only files changed since last backup
- Differential:
	- Backs up changes since last full backup

- Magnetic tape was standard for decades
- Cloud backups now widely used

# Grandfather-Father-Son Strategy
- Son:
	- Daily
	
- Father:
	- Weekly
	
- Grandfather:
	- Monthly

# Redundant Sites for Disaster Recovery
- Hot Site:
	- Fully equipped, live duplicate of original site. Instant failover possible
- Cold Site:
	- Empty facility with power and space. Equipment must be installed
- Warm Site:
	- Equipment is installed, but lacks active connections or updated data

[[Business Continuity]]
[[Redundant Sites]]

# Short QNA
- **What is business continuity?**  
    Business continuity is an organization’s ability to **maintain essential operations during and after** a disruptive event such as a natural disaster or cyberattack.
    
- **What is the purpose of a Business Continuity Plan (BCP)?**  
    A BCP provides **strategies, procedures, and resources** to ensure that key business functions can continue or quickly resume during disruptions.
    
- **List two examples of events that might trigger a business continuity plan.**  
    Examples include **earthquakes** and **cyberattacks**.
    
- **What is succession planning in business continuity?**  
    Succession planning pre-defines **who takes over leadership** if a key person is unavailable, incapacitated, or deceased, ensuring decision-making continuity.
    
- **What does a Business Impact Analysis (BIA) identify?**  
    A BIA identifies **critical business functions** and **assesses the impact** of their loss to help prioritize recovery strategies.
    
- **Why is regular testing of a BCP important?**  
    Regular testing ensures the **effectiveness of the plan**, reveals gaps, and confirms that employees are prepared for real-world disruptions.
    
- **What are the five W’s of a backup strategy?**  
    The five W’s are: **What** to back up, **When** to do it, **Where** to store it, **Which** media to use, and **Who** or what tool performs the backup.
    
- **What is the difference between a full backup and an incremental backup?**  
    A **full backup** copies all selected files, while an **incremental backup** only copies files changed since the last backup.
    
- **What is a hot site in disaster recovery?**  
    A **hot site** is a fully equipped, live duplicate of the original site that allows for **instant failover** during a disaster.
    
- **What does the Grandfather-Father-Son backup strategy refer to?**  
    It refers to a backup rotation schedule: **Son (daily), Father (weekly), and Grandfather (monthly)**.

# Long QNA
1. **Explain the concept of business continuity and why it is vital for organizations.**  
    Business continuity is the strategic approach that enables an organization to **continue delivering key operations** during and after disruptive events such as natural disasters, system failures, or cyberattacks. It is vital because it ensures that the business can **minimize downtime, protect assets, maintain customer trust**, and **avoid financial loss**. Without an effective continuity plan, even a brief disruption can have severe long-term impacts on a company’s operations and reputation.
    
2. **Describe the key steps involved in business continuity planning and testing.**  
    The business continuity planning process involves:
    
    1. **Identifying threats and exposures** that could disrupt business operations.
        
    2. **Creating prevention and recovery procedures** tailored to specific scenarios.
        
    3. **Testing and evaluating** the plan to ensure its effectiveness.
        
    4. **Training employees** so they understand their roles during a disruption.
        
    5. **Regularly updating** the plan to reflect changes in business operations, technology, and risk.  
        This structured approach ensures readiness and responsiveness in times of crisis.
        
3. **What is a Business Impact Analysis (BIA) and how does it support business continuity?**  
    A Business Impact Analysis (BIA) is a process that **identifies critical business functions**, evaluates the consequences of their disruption, and **prioritizes recovery efforts**. It helps organizations assess potential threats, such as system outages or supply chain failures, and determine the **financial and operational impact** of downtime. By aligning recovery plans with business priorities, a BIA ensures that the **most vital functions are restored first**, supporting an effective continuity strategy.
    
4. **Compare and contrast hot, cold, and warm sites used in disaster recovery.**
    
    - A **hot site** is a **fully operational duplicate** of the original site with real-time data and systems, allowing for **immediate recovery** with minimal downtime.
        
    - A **cold site** is a **bare facility** with space and power but no installed equipment or data, making it the **least expensive but slowest** to become operational.
        
    - A **warm site** falls in between—it has **pre-installed equipment** but lacks real-time data and active connections, requiring some configuration before use.  
        The choice depends on the organization's **budget, recovery time objectives (RTO), and criticality of services**.
        
5. **Explain the Grandfather-Father-Son backup strategy and its role in data retention.**  
    The Grandfather-Father-Son backup strategy is a **tiered backup rotation system** designed to maintain multiple levels of data recovery.
    
    - **Son** backups are taken **daily**,
        
    - **Father** backups are **weekly**,
        
    - and **Grandfather** backups are **monthly**.  
        This system ensures **multiple restore points** across different time frames, reducing the risk of data loss due to corruption or failure. It balances **storage efficiency, version control, and long-term data retention**, making it a foundational method in robust backup planning.