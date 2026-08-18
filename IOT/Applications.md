---
onenote-id: 0-c78d0179b8f94984976b812fcaf90787!1-D084F068F621FF9!3928
---
M2M  
Machine-to-Machine
 
- Automated interactions between devices
- IoT umbrella term for real world data collection, communication, processing and interactions

![Machine generated alternative text command Actuato...](../../../../img/OneNote/Applications%20image%20274a00c745b287cd.png)

Change Detection
 
_It refers to identifying times in which variations in the statistical properties (e.g. mean, variance) of data streams are detected as soon as they occur_
 
- Applications
	- Fire/fault detection
	- Auto segmentation
	- Activity recognition
	- Environmental monitoring
	- Quality control
- Cumulative Sum
	- CUSUM
	- Divide data into fixed size windows
	- Each window has mean
	- Analyse mean movement
- Data Reduction Prediction-based Approach
	- Predict model for results
	- Send to receiver
	- See how close model is to reality
	- Only send data if greater than error threshold
	- Limitations
		- Sender battery depletes
			- Keeps assuming values
		- Bad model
			- Use less sampling instead

Sigfox
 
- IoT generally short-range
- Narrowband
	- (Ultra-)
- Binary phase-shift keying
	- BPSK
	- Standard radio transmission method
	- Narrow chunks of spectrum and changes phase of carrier to encode
	- Receiver only listed to tiny slice
		- Mitigates noise
- Inexpensive endpoint radio
	- Sophisticated base-station
		- 100km
- Bidirectional
	- Base-station to endpoint is constrained

LoRa
 
- Spread-spectrum
	- \> 125 kHz
- LoRaWAN
	- Wider spectrum than SigFox
	- Elevated noise due to higher bandwidth mitigated by coding gains
	- Cheaper base-station than Sigfox
	- 27 kbps
- Endpoint and base-station inexpensive
	- Same radio
- Long-range transmission
	- 10 km in rural areas
- 50 kbps using FSK

Smart Cities
 
- Traffic management
- Waste management
- City transport
- Noise, air-quality control and monitoring
- Emergency services
- Security and safety
- Infrastructure management
- Elderly-care and social care−Smart metering

Traffic Control
 
- Sensors
	- Video
	- Sonar
	- Radar
	- Inductive Loops
	- Beacons
- Congestion control
	- Counting cars
		- Estimating speed
- Environmental factor can affect data
	- Fog for video
 
1. Design for large-scale and provide tools and APIs
2. Who will use data, how
3. How to update and change the data model
	1. And processing methods
4. Design for different audiences
	1. Consumers, developers
5. Data governance and privacy