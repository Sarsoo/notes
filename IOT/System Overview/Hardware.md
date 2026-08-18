---
onenote-id: 0-5405fbfec5f243aa884de0f2ea45143b!1-D084F068F621FF9!3928
---
Arduino
 
- Open-source
- User community
	- Design and manufacture kits
- Sensing and actuation

Intel Edison
 
- Embedded IoT platform
- High performance
- Wi-fi/Bluetooth
- 1 GB RAM
- 4 GB Storage

Libelium WASP Mote
 
- Microcontroller

Raspberry Pi
 
- Full Linux environment

Remote
 
- Wireless transceiver combined with sensors
	- Sensor node
- Addressability
	- Uniquely identifiable and findable
	- Managed by Identify of Things
		- IDoT
- 4 Components
	1. Sensors & Actuators
	2. Microcontroller & Memory
	3. Communication unit
	4. Power supply
		- Typically battery powered
		- Consumption typically main design issue
- Small size
- Low cost
- Not complicated tasks
- Two Types
	- Ready-to-deploy
		- Microcontroller
		- Onboard sensors
		- Sometimes standard interfaces for other sensors
		- E.g. Mote, Libelium
		- Pros
			- Rapid deployment
			- Not much hardware knowledge
		- Cons
			- Hard to customise
			- Proprietary dev environment
	- Baseboard
		- Only processing & communications
		- Some have common sensors
		- Need to add required sensors
		- E.g.
			- Raspberry Pi (zero)
			- Arduino
		- Pros
			- Flexible
			- Customisable
		- Cons
			- Hardware knowledge required
			- Limited firmware features
	- Single-board Computer
		- E.g. Raspberry Pi
		- Pros
			- Flexible
			- Feature rich OS
			- Powerful processor
		- Cons
			- Hardware knowledge

XM1000
 
- 16-bit RISC
- 8KB RAM
- ADC
	- 8 channels
- Sensors
	- 2x Light sensors
	- Temp and humidity
- Power
	- Multiple power profiles
		- MCU on
			- 1.8 mA constantly
		- MCU idle
			- CPU clock stopped
			- 54 μA
		- MCU standby
			- Entire MCU frozen
			- 5.1μA
	- 2 AA batteries
		- 3 V

![Time ms](../../../../../img/OneNote/Hardware%20image%2044493da114a1c65f.png)  

- During packet transmission
