**Authentication
- Definition: The process of <mark style="background: #ABF7F7A6;">verifying the identity of a user, device, or system</mark> to ensure that they are who they claim to be
- How it works: Authentication requires the user to <mark style="background: #ABF7F7A6;">provide credentials</mark> such as <mark style="background: #ABF7F7A6;">passwords</mark>, <mark style="background: #ABF7F7A6;">biometrics</mark> (fingerprints, face recognition), <mark style="background: #ABF7F7A6;">tokens</mark>, or <mark style="background: #ABF7F7A6;">certificates</mark>
- - **Types of Authentication:**
    - **Single-Factor Authentication <mark style="background: #ABF7F7A6;">(SFA)</mark>:** Uses <mark style="background: #ABF7F7A6;">one form of authentication</mark> (e.g., a password)
    - **Multi-Factor Authentication <mark style="background: #ABF7F7A6;">(MFA)</mark>:** Requires <mark style="background: #ABF7F7A6;">two or more independent credentials</mark> (e.g., a password and a fingerprint)
    - **Two-Factor Authentication <mark style="background: #ABF7F7A6;">(2FA)</mark>:** A <mark style="background: #ABF7F7A6;">specific form of MFA</mark> that <mark style="background: #ABF7F7A6;">requires exactly two methods</mark>, like <mark style="background: #ABF7F7A6;">a password and a one-time code sent via SMS</mark>
- **Example:** When logging into an online banking system, you must enter your username and password, and possibly a code sent to your phone (MFA)

**Authorisation
- **Definition:** The process of <mark style="background: #ABF7F7A6;">determining whether an authenticated user or system</mark> has <mark style="background: #ABF7F7A6;">permission to access</mark> certain resources or perform specific actions
- **How it works:** Once the <mark style="background: #ABF7F7A6;">user's identity is verified</mark>, the system checks their <mark style="background: #ABF7F7A6;">access rights</mark> to determine what <mark style="background: #ABF7F7A6;">resources they can use (files, systems, applications)</mark> and what <mark style="background: #ABF7F7A6;">actions they can perform (read, write, delete, execute)</mark>
- **Types of Authorization:**
    - **Role-Based Access Control <mark style="background: #ABF7F7A6;">(RBAC)</mark>:** Access rights are assigned based on the <mark style="background: #ABF7F7A6;">user's role within the organization</mark> (e.g., manager, employee, administrator)
    - **Access Control Lists <mark style="background: #ABF7F7A6;">(ACLs)</mark>:** Specifies which <mark style="background: #ABF7F7A6;">users or systems are granted access</mark> to <mark style="background: #ABF7F7A6;">objects (e.g., files, directories)</mark> and the <mark style="background: #ABF7F7A6;">operations they can perform on those objects</mark>
- **Example:** A user authenticated into a company’s intranet can access certain documents but may not have the necessary permissions to edit or delete them, based on their role

**Accounting (for Audit)
- **Definition:** The process of <mark style="background: #ABF7F7A6;">tracking and recording the actions or usage of resources</mark> by users or systems for <mark style="background: #ABF7F7A6;">auditing, monitoring, and reporting purposes</mark>
- **How it works:** Accounting ensures that <mark style="background: #ABF7F7A6;">all activities (logins, file access, changes)</mark> are <mark style="background: #ABF7F7A6;">logged and traceable</mark>, which can be reviewed later for compliance or to detect suspicious behavior
- **Example:** Logging user activity on a server to monitor who accessed sensitive data or when a critical system configuration was changed
- **Tools for Accounting:**
    - **Log Files:** Record all events and actions.
    - **Audit Trails:** Provide a chronological record of system activities for later analysis
    - **Monitoring Software:** Tools that actively track user and system activities in real-time


### **How AAA Works Together:**

1. **Authentication:** First, a user logs in (or authenticates) to the system using valid credentials.
2. **Authorization:** Once authenticated, the system checks what resources or actions the user is authorized to access or perform.
3. **Accounting:** Every action the user takes (e.g., accessing files, modifying settings) is logged for monitoring and auditing purposes.

### **Importance of AAA:**

- **Security:** Ensures that only authenticated and authorized users can access systems, minimizing the risk of unauthorized access.
- **Auditability:** Provides a traceable record of all actions, helping to detect malicious activity or errors.
- **Compliance:** Supports regulatory requirements that mandate the logging and monitoring of access to sensitive information.