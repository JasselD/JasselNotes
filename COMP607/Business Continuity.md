- <mark style="background: #ABF7F7A6;">Strategies and processes</mark> to ensure that <mark style="background: #ABF7F7A6;">critical business operations continue</mark> even <mark style="background: #ABF7F7A6;">during disruptions</mark> like hardware failure, natural disasters, or cyberattacks

**Clustering:
- <mark style="background: #ABF7F7A6;">Server cluster</mark>:
	- <mark style="background: #ABF7F7A6;">Group of independent servers</mark> working together to provide <mark style="background: #ABF7F7A6;">high availability and load balancing</mark> for application and services
	- They <mark style="background: #ABF7F7A6;">operate in tandem</mark> to ensure the service <mark style="background: #ABF7F7A6;">remains available even if one or more server fails</mark>
	- Example: If one web server goes offline, others can handle the traffic
- <mark style="background: #ABF7F7A6;">Public cluster connection</mark>:
	- <mark style="background: #ABF7F7A6;">Network interface</mark> that<mark style="background: #ABF7F7A6;"> handles traffic</mark> between the <mark style="background: #ABF7F7A6;">cluster and external clients</mark>
	- Purpose: External or public-facing connection through which clients access the services provided by the cluster
	- Example:<mark style="background: #ABF7F7A6;"> Load balancer or virtual IP add is typically used</mark> to <mark style="background: #ABF7F7A6;">distribute the incoming traffic</mark> among the nodes in the cluster
- Private cluster connection:
	- Dedicated network interface used exclusively for internal communication between the server (nodes) in a cluster
	- Purpose: Allows cluster nodes to synchronize data, check each other's status, and coordinate actions like failover or workload distribution
	- Example: In a database cluster, the private cluster connection enables the replication of data between nodes and ensure that all the servers stay in sync

**How public and private cluster connections work together
- Public cluster connection: Handles all external traffic, such as users accessing a web application or service
- Private cluster connection: Manages internal communications, such as data replication, health checks, and failover coordination

**Server Redundancy
- Types:
	- Cold redundancy: Backup servers are turned off until need. There's a downtime while they start up
	- Warm redundancy: Backup servers are on standby and can quickly take over if needed, with minimal delay
	- Hot redundancy: Backup servers are fully active and synchorized with primary server. They take over instantly if the primary fails

