- Thin software layer
- Basic programming abstractions
- Interact with hardware
	- Schedule and prioritise tasks
- Mediate between applications and services requiring resources
[Comparison of Operating Systems TinyOS and Contiki](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.636.3680&rep=rep1&type=pdf)

# Environment
- Energy efficiency
- Restricted code
	- Compared to full OS

# Features
- Memory management
- Power management
- File management
- Networking
- Dev environment and tools
	- Commands
	- Interpreters
	- Compilers
- Entry points for sensitive resources
	- Input components
- Functional aspects
	- Scheduling
	- Multi-threading
	- Interrupts
	- Memory allocation

# Dynamic Programming
- Program parts of application after deployment
	- Settings and requirements not known prior to deployment
		- Can change over time
	- Bug fixes or update requirements wile in operation
	- Manual updates maybe not possible
- Needs boundaries between application and OS
- OS receive software updates and store in active memory
	- Check this is an updated version
	- Install and configure new version

# Paradigm
- Node-centric
	- Focuses on software for each node
	- Operating individually
- Application-centric
	- Treat nodes as one application
	- Requires collaboration between nodes
		- Collection
		- Dissemination
		- Analysis and/or processing of generated and collected data

# Deploy to Mote
- Compile
	- make TARGET=xm1000 _____
- Deploy
	- make TARGET=xm1000 _____.upload
		- As root
- Terminal
	- make TARGET=xm1000 login

# TinyOS
*Embedded, component-based operating system and platform for low-power wireless devices, such as those used in [wireless sensor networks](https://en.wikipedia.org/wiki/Wireless_sensor_network) (WSNs), [smartdust](https://en.wikipedia.org/wiki/Smartdust), [ubiquitous computing](https://en.wikipedia.org/wiki/Ubiquitous_computing), [personal area networks](https://en.wikipedia.org/wiki/Personal_area_network), [building automation](https://en.wikipedia.org/wiki/Building_automation), and [smart meters](https://en.wikipedia.org/wiki/Smart_meter)*

From <[https://en.wikipedia.org/wiki/TinyOS](https://en.wikipedia.org/wiki/TinyOS)>

- Written in nesC
	- Network Embedded Systems C
	- Component-based
		- Wired together to run applications
	- Event-driven
	- Extension to C
- Non-blocking
	- One stack
	- No abstraction between OS and application
- No dynamic programming
- I/O ops longer than hundreds of milliseconds are async
- Mainly event-based

# FreeRTOS
- Minimal ROM, RAM, processing overhead
- Bin image 6K - 12K
- 3 C files
- Smaller & easier real-time processing alternative
- Port layer
	- Architecture specific part of port
	- Officially supported or contributed
- Good for AWS