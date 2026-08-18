---
onenote-id: 0-e705d268e8a643a0a0dd079d81d06afd!1-D084F068F621FF9!3928
---
- Wired
	- USB
	- Ethernet
- Wireless
	- Wi-Fi
	- Bluetooth
	- Zigbee
	- IEEE 802.15.x
- Single-hop/Multi-hop
	- Sink nodes
	- Cluster heads
- Point-to-Point/Point-to-Multi-Point

Zigbee
 
- Low cost
- Low power
- Mesh network
- Industrial, scientific, medical radio bands
- PHY/MAC layers based on IEEE 802.15.4
- Sleep to active
	- \< 30ms
	- Quicker than Bluetooth (\< 5.1)
 ![APPLICATIONPROFILES APPLICATION FRAMEWORK NETWORFJ...](../../../../../img/OneNote/Net-App%20Layers%20image%201ff07ca7f302fc5b.png)

Network Layer 3
 
- IPv4
	- Gateway or middleware
	- Inefficient for embedded
	- Low bit rate
	- Constrained power
- IPv6
	- Overhead
	- Larger header
	- 6LowPAN

6LowPan  
IPv6 over Low Power Wireless Personal Area Networks
 
_Encapsulation and header compression mechanisms that allow IPv6 packets to be sent and received over_ _IEEE 802.15.4_ _based networks_
 \> From \<[https://en.wikipedia.org/wiki/6LoWPAN](https://en.wikipedia.org/wiki/6LoWPAN)\>   
- Good for IoT
- Small packet size
	- 127 bytes
- Header compression
- Fragmentation and reassembly
	- Different types by device type
- 16-bit or IEEE 64-bit extended MAC addresses
- IPv6 MTU 1280 octets
	- IEEE 802.15.4 MTU 127 octets
- Low bandwidth
	- 250 kbps
		- 2.4 GHz
	- 40 kbps
		- 915 MHz
	- 20 kbps
		- 868 MHz

Gateway/Middleware
 
- Not realistic to have all IoT devices IP-enabled
- Gateway
	- QoS
	- Caching
	- Mechanisms to address heterogeneity/interoperability
 ![Internet IPv6 6LowPAN Sensor Device 6LowPAN NonIP ...](../../../../../img/OneNote/Net-App%20Layers%20image%207822e2de99ca20d0.png)

CoAP  
Constrained Application Protocol
 
- Transfer protocol
- Constrained nodes and networks
- REST architecture
	- Resources at URIs
	- Verbs
- HTTP too slow
- UDP instead of TCP
	- Simple "message layer" for re-transmission
- Compression
 ![Server GETtemperature, Room A Client 200 OK Txtpla...](../../../../../img/OneNote/Net-App%20Layers%20image%20923694bedc78090d.png)  
![Node Server proxy c c coAP c H TTP TCP Ethernet li...](../../../../../img/OneNote/Net-App%20Layers%20image%206bbea49abf52b5bf.png)

|   |   |
|---|---|
|Protocol|Layer|
|CoAP|Application|
|6LoWPAN|Network/IP|
|IEEE 802.15.4|MAC|
|IEEE 802.15.4|Physical|
 
MQTT  
MQ Telemetry Transport
 
- Lightweight
	- Good for constrained environments
	- 2 byte fixed header
- Optional variable-length header
- Optional payload
- One-to-[one/many]
- Delivery
	- At Most Once
		- Noisy environment
		- Best effort of TCP/IP
		- Loss or duplication possible
		- E.g. Ambient sensor data
			- Not critical if a measurement is lost
	- At Least Once
		- Assured to arrive
			- More than one possible
	- Exactly Once
		- Good for billing
 ![byte 1 byte 2 MQTT Control Packet type 3 DUP nag Q...](../../../../../img/OneNote/Net-App%20Layers%20image%207050e8393822db6e.png)

- DUP
	- Duplicate
	- At most/least once
- RETAIN
	- Only for publish
	- 1
		- Hold for future subscribers
		- Last known good value
 ![QOS Val Al most once delivery R least mce delivery...](../../../../../img/OneNote/Net-App%20Layers%20image%20d1c91a4c8c300d04.png)  
![Exported image](../../../../../img/OneNote/Net-App%20Layers%20image%20b834c0fcbe255d02.png)

Pub/Sub
 
- Message bus
 ![Software bus](../../../../../img/OneNote/Net-App%20Layers%20image%20258114e527a3127f.png)  

- RabbitMQ
- Protocols
	- AMQP
	- MQTT
- Terms
	- Producer
	- Queue
	- Consumer

[Solace MQTT](https://docs.solace.com/MQTT-311-Prtl-Conformance-Spec/MQTT%20Control%20Packet%20format.htm)  
[Solace MQTT Fixed Header](https://docs.solace.com/MQTT-311-Prtl-Conformance-Spec/MQTT%20Control%20Packets.htm#_Ref384201650)

