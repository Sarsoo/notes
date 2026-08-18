---
onenote-id: 0-dd9d5d83881047e98f25c78780645ff9!1-D084F068F621FF9!3928
---
Source Routing
 
- Source takes control of forwarding
- Constantly flood with request
	- Attach address to info in header
	- Only if path is better
 
# Route Request RREQ

![Source ABD ABD Destination ABE ABEF](../../../../../img/OneNote/Routing%20image%20d3a28c10b1ed32aa.png)  

# Route Reply RREP

![Source ABD Destination](../../../../../img/OneNote/Routing%20image%209bd27878a9383ad4.png)

Ad Hoc On-Demand Distance Vector
 
# RREQ

![RREQ Source c route entry for A To A, 1 hop, via A...](../../../../../img/OneNote/Routing%20image%207cfc16ab9b609be6.png)  

# RREP

![To A, Source c To A, 1 hop, via A 1 hop, 2 hops, v...](../../../../../img/OneNote/Routing%20image%20d31fcb451380861a.png)  

- Distance vector maintenance
	- Purge entries after a while
	- Stale
 
# Enhancements

- Intermediate nodes reply RREP on destination behalf
- Packet sequence numbers to reduce rebroadcasts
- Set TTL

IPv6 Routing Protocol for Low-Power & Lossy Networks  
RPL
 
- Distance vector
- Proactive
- Multiple routes
- Destination Oriented Directed Acyclic Graph
	- DODAG
	- Destination-oriented
		- Single destination
	- Directed Acyclic Graph
		- Directed graph without loops
 
# DODAG Building

- Node designated root
- Control messages created
	- DIS
		- Information solicitation
	- DIO
		- Information object
	- DAO
		- Destination advertisement object
- Objective Function (OF)
	- Specified for each node to compute rank
- Turn network topology into tree
 
### At the Root

- Periodically broadcasts DIO to neighbours

### Other nodes

- Receive DIO
	- Compute rank of received DIO based on Objective Function
	- Compare if rank is lower than seen before
		- If lower, keep that as lowest
			- Broadcast DIO to neighbours
				- Flood DIO to network
			- Set preferred parent to node that sent it
		- If higher
			- Ignore
 ![Preferred Parent B DIO ROOT E Preferred Parent DIO...](../../../../../img/OneNote/Routing%20image%2095b8b5810f3c5c27.png)  
![Preferred Parent Preferred Parent B Preferred Pare...](../../../../../img/OneNote/Routing%20image%2036c5b5880a19c75e.png)  

- Defines best path for upward (to root) transmission
 
# Downward Transmission

### Point-to-Multi-Point (P2MP)

- Source routing
	- Each node sends DAO to root
	- Each node appends ID
		- Relays DAO
	- Construct subtree for downward traffic
		- Storing node
			- Otherwise non-storing
	- Root builds complete tree for downward traffic
		- Use source routing
 
### Point-to-Point (P2P)

- Between any pair of nodes
	- Upward to root
	- Downward from root
 
# Topology Maintenance

- Prune too frequently
	- Waste if radio & battery resources
- Not frequently enough
	- Routing may be unstable
- Trickle timer used
	- Node periodically transmits data
		- Unless other nodes are redundant
	- When routing inconsistencies detected
		- Loops, loss of parent
		- Trickle timer reset
			- Fix quickly

# Stage 1: Route Discovery via Flooding

- The **SOURCE** broadcasts a **REQUEST** message, the message contains a field for each node to fill the path information
- Each node includes its address in path info of the **REQUEST** message, and rebroadcasts **REQUEST** only if the REQUEST represents a better path (e.g. least number of hops)
- **REQUEST** will be flooded in the network and will reach the **DESTINATION**. The path info will contain all nodes from the **SOURCE** to the **DESTINATION** hop-by-hop
 
# Stage 2: Route Reply via Unicast

- Upon receiving the **REQUEST** message, the **DESTINATION** retrieves the path info from **REQUEST**
- The **DESTINATION** constructs a **REPLY** message including the received path info, and identify the next hop to unicast **REPLY**
- Each node receiving **REPLY** refers to the path info in the message to forward the **REPLY** to its next hop
- The **REPLY** message will eventually reach the **SOURCE**. The **SOURCE** then retrieves the path info for data transmission
 
# Stage 3: Packet Data Transmission

- The **SOURCE** includes the path info in the data packet, identify the next hop to unicast the packet
- Upon receiving the packet, each node refers to the path info in the packet to forward the packet to its next hop
- Since the path info describes the route from **SOURCE** to **DESTINATION** hop-by-hop, the packet will be forwarded in the network by each node to reach the **DESTINATION**

# Stage 1: Route Discovery via Flooding

- The **SOURCE** broadcasts a **REQUEST** message, called RREQ
- Upon receiving RREQ, each node rebroadcasts the RREQ &amp; creates a **ROUTE ENTRY** based on the following knowledge:
	- i.e. Say Node-S initiates RREQ, and the RREQ reaches Node-A from Node-R, then Node-A will know that all packets addressing to Node-S can be handled by Node-R
- RREQ will be flooded in the network and will eventually reach the **DESTINATION**
 
# Stage 2: Route Reply via Unicast

- Upon receiving the **REQUEST** message, the **DESTINATION** constructs a RREP (Route Response) message
- Based on the **ROUTE ENTRY** built during the RREQ flooding, each node unicasts the receiving RREP back to the SOURCE and creates the corresponding **ROUTE ENTRY** for the **DESTINATION**
- The RREP message will eventually reach the **SOURCE**. The **SOURCE** will build the corresponding **ROUTE ENTRY** and use it to perform data packet transmission
 
# Stage 3: Packet Data Transmission

- As all involved nodes have created the **ROUTE ENTRY** for the **SOURCE** & **DESTINATION** locally, they have the knowledge to forward packets addressing to either **SOURCE** or **DESTINATION**
- The packet forwarding is based on the next hop information recorded in the **ROUTE ENTRY**

- Pass packets between nodes to get to gateway
- Best node maintained in routing table
- How to build
	- Link state
		- Dijkstra's algorithm
		- Popular in wired and OSPF
		- Not big in IoT
	- Distance vector
		- Work out distances to other nodes
- When to build
	- Proactive
		- Table-driven
		- Periodically pass info between nodes
		- Can send packet immediately
		- Suited to static topology
	- Reactive
		- On-demand
		- Does route discovery before sending packet
		- Route table created at party nodes
		- Cache table
		- Suited to dynamic topology
 
# Table-less Routing

- Flooding
	- Send to all
- Source Routing
	- Send routing information with packet header
	- Intermediate don't need a routing table
 
# IoT Specific

- Ad hoc On-demand Distance Vector (AODV)
	- Zigbee
- IPv6 Routing Protocol (RPL) for Low-Power & Lossy Networks
	- Contiki OS, TinyOS
 
Mesh-under vs Route-over
 
- Packets can be relayed in different ways
- Layer-2 Switching
	- Mesh-under
	- Single layer-2 domain
		- Multiple star topologies meshed together
	- Packets forwarded by L2
	- Simpler solution & lower transmission delay
- Layer-3 Routing
	- Route-over
	- Separates data link & routing
	- Agnostic to PHY/MAC
	- Better management of larger networks
