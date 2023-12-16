
# [Load Balancing](https://www.nginx.com/resources/glossary/load-balancing/)

## What is Load Balancing?

**Load balancing** refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.

High-Traffic Websites must serve hundreads of thousands, if not millions, of concurrent requests from users or clients and return the correct text, images, video, or application data, all in a fast and reliable manner. To cost-effectively scale to meet these high volumes, modern computing best practise generally requires adding more servers.

A **load balancer** acts as the "traffic cop" sitting in front of your servers and routing client requests acroos all servers capable of fulfilling thos requests in a manner that maximizes speed and capacity utilization and ensures that no one server is overworked, which could degrade performance. If a single server goes down, the load balancer redirects traffic to the remaning online servers. When a new server is added to the server group, the load balancer automatically starts to send requests to it.

**Functions of a Load Balancer**
- Distributes client requests or network load efficiently across multiple servers
- Ensure high availability and reliability by sending requests only to servers that are online
- Provides the flexibility to add or subtract servers as demand dictates

![load balancing diagram]()

### How does Load Balancing work?

Load balancing is handled by a tool or application called a load balancer. A load balancer can be either hardware-based or software-based. Hardware load balancers require the installation of a dedicated load balancing device; software-based load balancers can run on a server, on a virtual machine, or in the cloud. Content delivery networks (CDN) often include load balancing features.

### Static Load Balancing Algorithms

Static load balancing algorithms distribute workloads without taking into account the current state of the system. A static load balancer will not be aware of which servers are performing slowly and which servers are not being used enough. Instead it assigns workloads based on a predetermined plan. Static load balancing is quick to set up, but can result in inefficiencies.

### Dynamic Load Balancing Algorithms

Dynamic load balancing algorithms take the current availability, workload, and health of each server into account. They can shift traffic from overburdened or poorly performing servers to underutilized servers, keeping the distribution even and efficient. However, dynamic load balancing is more difficult to configure. A number of different factors play into server availability: the health and overall capacity of each server, the size of the tasks being distributed, and so on.

### Server Monitoring and Failover

**Server Monitoring**

Dynamic load balancers must be aware of server health: their current status, how well they are performing, etc. Dynamic load balancers monitor servers by performing regular server health checks. If a server or group of servers is performing slowly, the load balancer distributes less traffic to it. If a server or group of servers fails completely, the load balancer reroutes traffic to another group of servers, a process known as "failover."

**Failover**

Failover occurs when a given server is not functioning and a load balancer distributes its normal processes to a secondary server or group of servers. Server failover is crucial for reliability: if there is no backup in place, a server crash could bring down a website or application. It is important that failover takes place quickly to avoid a gap in service.

### Load Balancing Algorithms

Different load balancing algorithms provide benefits; the choice of load balancing methos depends on your needs:

- **Round Robin** -- Requests are distributed across the group of servers sequentially.
- **Least Connections** -- A new request is sent to the server with the fewest current connections to clients. The relative computing capacity of each server is factored into determining which one had the least connections.
- **Least Time** -- Sends a requests to the server selected by a formula that combines the fastest response time and fewest active connections. Exclusive to NGINX plus.
- **Hash** -- Distributes requests based on a key you define, such as the client IP address or the request URL, NGINX Plus can optionally apply a consistent hash to minimize redistribution of loads if the set of upstream servers changes.
- **IP Hash** -- The IP address of the client is used to determine which server receieves the request.
- **Random with Two Choices** -- Picks two servers at random and sends the request to the one that is selected by then applying the Least Connections algorithms (or for NGINX Plus the Least Time algorithm, if so configured).
 
### Benefits of Load Balancing

- Reduce downtime
- Scalable
- Redundancy
- Flexibility
- Efficiency

### Related Topics

**Session Persistence**

Information about a user's session is often stored locally in the browser. For example, in a shopping cart application the items in a user's cart might be stored at the browser level until the user is ready to purchase them. Changing which server receives requests from that client in the middle of the shopping session can cause performance issues or outright transaction failure. In such cases, it is essential that all requests from a client are sent to the same server for the duration of the session. This is known as session persistence.


**Dynamic Configuration of Server Groups**

Many fast-changing applications require new server to be added or taken down on a constant basis. This is common in environments such as the Amazon Web Services (AWS) Elastic Compute Cloud (EC2), which enables users to pay only for the computing capacity they actually use, while at the same time ensuring that capacity scales up in response traffic spikes. In such environments it greatly helps if the load balancer can dynamically add or remove servers from the group without interrupting existing connections.

**Hardware vs. Software Load Balancing**

Load balancers typically come in two flavors: hardware-based and software-based. Vendors of hardware-based solutions load proprietary software onto the machine they provide, which often uses specialized processors. To cope with increasing traffic at your website, you have to buy more or bigger machines from the vendor. Software solutions generally run on commodity hardware, making them less expensive and more flexible. You can install the software on the hardware of your choice or in cloud environments like AWS EC2.

**Seven-Layer Open System Interconnection (OSI)**

Load balancing can be performed at various layers in the Open Systems Interconnection (OSI) Reference Model for networking.
Layer 7 load balancing is more CPU‑intensive than packet‑based Layer 4 load balancing, but rarely causes degraded performance on a modern server. Layer 7 load balancing enables the load balancer to make smarter load‑balancing decisions, and to apply optimizations and changes to the content.
