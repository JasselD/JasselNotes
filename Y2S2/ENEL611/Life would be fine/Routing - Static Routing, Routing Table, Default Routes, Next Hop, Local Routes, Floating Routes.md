# Routing
- What?
	- Process of forwarding data from a source to a destination across different networks. Routers use routing tables to make forwarding decisions and determine the best path for the data to travel

# Static Routing
- What?
	- Static Routing involves manually configuring routes on a router. The administrator specific the destination network and the next-hop IP address for exit interface to reach that network
	
	- Unlike dynamic routing, which uses protocols like OSPF or EIGRP to automatically learn routes, static routing requires manual configuration and is fixed unless modified
	
- Why?
	- Simplicity:
		- Static routes are easy to configure and do not require complex protocols
		
	- Control:
		- You have full control over the routes and can fine-tune network traffic paths
		
	- Security:
		- Static routes are less susceptible to routing attacks (e.g, route poisoning) because no dynamic updates are received from other routers

# Routing Table
- What?
	- Routing table contains all the routes that a router knows about, either through static routes, dynamic routing protocols, or directly connected networks
	
	- Each entry in the routing table consists of:
		- Destination network
		- Subnet network
		- Next-hop IP address or exit interface
		- Route source (whether the route was learned through static routing, dynamic routing, or directly connected)

# Default Routes
- What?
	- Default route is used when the route does not know how to reach a specific destination in the routing table. It acts as a catch-all route and forwards traffic to a specified next hop when no other matching routes exist
	- The default route is commonly referred to as the "gateway of last resort"
	
- When?
	- Use a default route when a router is connected to the Internet or to an external network where it needs to forward traffic to any destination that is not in the local routing table

# Next Hop
- What?
	- The next hop is the next router or device that a packet must pass through to reach its final destination. In static routing, the next hop is specified as the next hop IP address

# Local Routes
- What?
	- A local route is a route that is directly configured on the  router's interface. It is a route to the network that is directly connected to the router
	
- How to view?
	- Local routes can be viewed in the routing table used ther C (connected) code. They do not require static configuration because the router automatically knows about them

# Floating Routes
- What?
	- A floating route is a backup route that is configured with a higher administrative distance (AD) than the primary route. The route will only be used if the primary route fails
	
	- The administrative distance defines the truthworthiness of a route. Lower values are more trusted (eg., directly connected routes have an AD of 0, while static routes have an AD of 1)
	
- Why?
	- Floating routes are useful for backup routes that are only used when the primary route is unavailable. This provides redundancy and fault tolerance in a network

## QNA
- **What is the difference between a default route and a floating route?**
    
    - A **default route** is a **catch-all route** used when no specific route matches the destination. A **floating route** is a **backup route** with a higher **administrative distance** that is only used if the primary route fails.
        
- **What is the purpose of the "next hop" in static routing?**
    
    - The **next hop** is the **next router** or device where packets should be forwarded in order to reach their final destination.