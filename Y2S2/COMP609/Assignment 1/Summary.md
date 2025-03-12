### **Company Overview**

- Industrial bakery producing **20,000 loaves of bread per day**.
- **26 staff** total, including:
    - 15 bakers (14 + 1 shop floor manager)
    - 1 manager (Mungo Campbell)
    - 1 accountant
    - 3 accounts clerks (Receivable, Payable, Payroll)
    - 1 sales manager
    - 1 salesman
    - 1 receptionist / telephonist / PA
    - 1 dispatch clerk
    - 2 delivery drivers

### **Products**

- **4 standard loaves**.
- **12 boutique varieties**.
- Clients include **dairies, specialty bread shops, supermarkets**.

### **Current Applications & Systems**

- **MS Office suite** (general office productivity).
- **MYOB** (accounting software).
- **Recipe Database** (SQL Server-based).
- **People Manager** (payroll system).
- **Oven control software** (3 separate PCs, **non-networked**, storing time/temp data in recipe DB)

### **Current Network Setup**

- **MS Peer-to-peer network** (unplanned, ad-hoc growth).
- **No real network design**—devices added without strategy.
- Some **desktops act as servers**.
- **Dedicated server** for MYOB and People Manager (but has **access issues**).
- **Sales manager has isolated MYOB copy** (order files unavailable unless he is present and PC is on).
- **Bakers need order printouts by 9 PM**, but **only sales manager and manager have office keys**—logistics issue.
- Ovens' PCs **isolated**, data transferred via **floppy disks** (prone to **corruption due to dust/flour**).
- **Internet and email server** recently added.
- **Amateur web server** running on the **email server** (improper configuration)

**Problems
- Access problems (give certain people access to certain things)
	- Give bakers special authorithy 
- Make it remote for Sales Manager
- Upgrade Ovens' PC from floppy disks
- Make infrastructure upgradable (future proof)
- Upgrade web server (fix configuration)