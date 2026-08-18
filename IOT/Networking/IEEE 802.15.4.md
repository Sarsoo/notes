---
onenote-id: 0-67b1c8af15db4920852631ac9638800d!1-D084F068F621FF9!3928
---
Low-Rate Wireless Personal Area Networks  
LR-WPAN
 
- Zigbee
- 6LoWPAN
 
- Includes PHY & MAC layer
- \< 250 kb/s
- Three possible frequency bands (unlicensed):
	- 868.0-868.6 MHz
	- 902-928 MHz
	- 2.4-2.485 GHz
 ![WiFi 16 channels 11 12 13 14 15 16 17 18 19 20 21 ...](../../../../../img/OneNote/IEEE%20802.15.4%20image%204ae02299519b57eb.png)  

- Overlap with Wi-Fi
- Tune all devices to same
 
# MAC Topology

- Star
	- ![Exported image](../../../../../img/OneNote/IEEE%20802.15.4%20image%20942016962bb6ce6f.png)
- Mesh
	- ![Exported image](../../../../../img/OneNote/IEEE%20802.15.4%20image%208deee5e4a6f044b6.png)
	- Orange, 1st PAN coordinator
		- Instructs device to become PAN coordinator of new cluster adjacent to first one
 
# Device classes

- FFD
	- Full function device
	- Can coordinate PAN
	- Communicate with any device
- RFD
	- Reduced function device
	- Only communicates with coordinator
   

Super-Frame
 
- For beacon mode
- Defines when node can access channel
 ![Battery life extension Contention Accdss Peridd GT...](../../../../../img/OneNote/IEEE%20802.15.4%20image%201beebb1b5cb2bf77.png)  
![15ms 2s0 where 0 s SO _ 14 15ms 280 where SO BO 14...](../../../../../img/OneNote/IEEE%20802.15.4%20image%209bff74f563cf080e.png)

- Turn radio off during inactive period
	- Tune duty-cycle
- Save energy
 
# GTS

- Guaranteed timeslot
- Contention-free access within super-frame
- Allocated by PAN coordinator
	- 7 at a time
	- Based on
		- GTS requests
		- Available capacity in super-frame
- Full functioning devices (FFD) can request fixed transmission rate
	- Need to track beacon

CSMA-CA
 
- Random access protocol
- Slotted
	- Battery extension
	- Sync with coordinator
	- Perform multiple CCAs to avoid collision with ACK
		- Clear Channel Assessment
- Unslotted
	- Node send packet when ready
	- On collision
		- Wait for period
			- Random back-off
		- Check channel for ongoing transmission
	- Counters
		- Number of Back-off
			- NB
		- Back-off Exponent
			- BE
			- Maintains back-off window

![Application Software implementation Application Su...](../../../../../img/OneNote/IEEE%20802.15.4%20image%20266e86fe8a3c1914.png)

Modes
 
- Beacon
	- Use coordinator to coordinate transmission
	- Transmits beacon to synchronise
		- All nodes are synchronized in time
	- Other nodes scan for beacon
		- Then use CSMA-CA to access super-frame on channel
			- Random delay when accessing
	- Contention free using Guaranteed Time Slots (GTS)
		- Assigned by coordinator
- Non-beacon
	- Point-to-point
	- Unslotted CSMA-CA
	- Less configuration
		- Must listen to channel continuously
- Data acknowledgement
	- ACK frames sent without CSMA-CA
		- No random delay
	- Timeout retransmission
		- For acknowledged transmission
	- Transmission always considered successful for unacknowledged transmission
 ![Beacon Mode data Network Coordinator Device Beacon...](../../../../../img/OneNote/IEEE%20802.15.4%20image%20418e21be2a34794f.png)  
![Beacon Mode data Network Coordinator Device Beacon...](../../../../../img/OneNote/IEEE%20802.15.4%20image%201ac4d787dfd76af2.png)