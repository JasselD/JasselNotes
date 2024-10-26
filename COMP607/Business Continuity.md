- Strategies and processes to ensure that critical business operations continue even during disruptions like hardware failure, natural disasters, or cyberattacks

Clustering:
- Server cluster:
	- Group of independent servers working together to provide high availability and load balancing for application and services
	- They operate in tandem to ensure the service remains available even if one or more server fails
	- Example: If one web server goes offline, others can handle the traffic
- Public cluster connection:
	- Network interface that handles traffic between the cluster and external clients
	- Purpose: External or public-facing connection through which clients access the services provided by the cluster
	- Example: Load balancer or virtual IP add is typically used to distribute the incoming traffic among the nodes in the cluster
- Private cluster connection:
	- Dedicated network interface used exclusively for internal communication between the server (nodes) in a cluster
	- Purpose: Allows cluster nodes to synchron