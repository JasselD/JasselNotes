- <mark style="background: #ABF7F7A6;">Strategies and processes</mark> to ensure that <mark style="background: #ABF7F7A6;">critical business operations continue</mark> even <mark style="background: #ABF7F7A6;">during disruptions</mark> like hardware failure, natural disasters, or cyberattacks

**Clustering:
- <mark style="background: #ABF7F7A6;">Server cluster</mark>:
	- <mark style="background: #ABF7F7A6;">Group of independent servers</mark> working together to provide <mark style="background: #ABF7F7A6;">high availability and load balancing</mark> for application and services
	- They <mark style="background: #ABF7F7A6;">operate in tandem</mark> to ensure the service <mark style="background: #ABF7F7A6;">remains available even if one or more server fails</mark>
	- Example: If one web server goes offline, others can handle the traffic
- <mark style="background: #ABF7F7A6;">Public cluster connection</mark>:
	- <mark style="background: #ABF7F7A6;">Network interface</mark> that <mark style="background: #ABF7F7A6;">handles traffic</mark> between the <mark style="background: #ABF7F7A6;">cluster and external clients</mark>
	- Purpose: External or public-facing connection through which clients access the services provided by the cluster
	- Example: <mark style="background: #ABF7F7A6;">Load balancer or virtual IP add is typically used</mark> to <mark style="background: #ABF7F7A6;">distribute the incoming traffic</mark> among the nodes in the cluster
- <mark style="background: #ABF7F7A6;">Private cluster connection</mark>:
	- <mark style="background: #ABF7F7A6;">Dedicated network interface</mark> used exclusively for <mark style="background: #ABF7F7A6;">internal communication</mark> between <mark style="background: #ABF7F7A6;">the server (nodes) in a cluster</mark>
	- Purpose: <mark style="background: #ABF7F7A6;">Allows cluster nodes to synchronize data</mark>, <mark style="background: #ABF7F7A6;">check each other's status</mark>, and <mark style="background: #ABF7F7A6;">coordinate actions</mark> like <mark style="background: #ABF7F7A6;">failover or workload distribution</mark>
	- Example: In a database cluster, the private cluster connection enables the <mark style="background: #ABF7F7A6;">replication of data between nodes</mark> and <mark style="background: #ABF7F7A6;">ensure that all the servers stay in sync</mark>

**How public and private cluster connections work together
- Public cluster connection: <mark style="background: #ABF7F7A6;">Handles all external traffic</mark>, such as users accessing a web application or service
- Private cluster connection: <mark style="background: #ABF7F7A6;">Manages internal communications</mark>, such as <mark style="background: #ABF7F7A6;">data replication</mark>, <mark style="background: #ABF7F7A6;">health checks</mark>, and <mark style="background: #ABF7F7A6;">failover coordination</mark>

**Server Redundancy
- Types:
	- Cold redundancy: Backup servers are <mark style="background: #ABF7F7A6;">turned off until needed</mark>. There's a <mark style="background: #ABF7F7A6;">downtime while they start up</mark>
	- Warm redundancy: Backup servers are on <mark style="background: #ABF7F7A6;">standby and can quickly take over if needed</mark>, with <mark style="background: #ABF7F7A6;">minimal delay</mark>
	- Hot redundancy: Backup servers are <mark style="background: #ABF7F7A6;">fully active and synchorized with primary server</mark>. They take over <mark style="background: #ABF7F7A6;">instantly</mark> if the primary fails

- [[Backup Types]]
- [[RAID]]
- [[Redundant Sites]]