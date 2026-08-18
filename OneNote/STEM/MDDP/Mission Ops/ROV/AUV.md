---
onenote-id: 0-b079dc5a213d072d127d42585be21f11!1-D084F068F621FF9!3684
---
For report

- Turn ROV into AUV
- [Wiki - Autonomous underwater vehicle](https://en.wikipedia.org/wiki/Autonomous_underwater_vehicle)
 
Untethered
 
[NOAA - What Are AUVs, and Why Do We Use Them?](https://oceanexplorer.noaa.gov/explorations/08auvfest/background/auvs/auvs.html)
 
[Box frame paper](https://ieeexplore.ieee.org/document/8729807)
 
[In place cable repair](https://www.n-sea.com/en/news/n-sea-completes-industry-first-subsea-repair-operation)
 
[Freedom Hybrid ROV/AUV](https://www.oceaneering.com/rov-services/next-generation-subsea-vehicles/freedom/)

- [Freedom presentation](https://www.sut.org/wp-content/uploads/2018/06/Aaron-Leather-v2-AUT-Freedom-Rev3-Final-Submission-draft-2-21.10.2019.pdf)
 
[Aquabotix hybrid AUV/ROV](https://www.unmannedsystemstechnology.com/2017/12/aquabotix-launches-hybrid-auvrov-system/)

Applications
 
# Commercial

- Map sea floor
	- Research for infrastructure
- Post-lay surveys
	- Inspection
 
# Research

- Variety of sensors
	- Concentration of whatever
	- Absorption or reflection of light
	- Microscopic life
	- Conductivity-temperature-depth
		- CTD
	- Fluorometer
	- pH
 
# Shifting drugs

# Air crash investigations

# Military

Companies
 
Kongsberg Maritime  
Bluefin Robotics  
Teledyne Gavia  
International Submarine Engineering  
Atlas Elektronik  
OceanScan

Navigation
 
Radio waves can’t penetrate very far

- No GPS
 
# Dead Reckoning

- Work relative from known fixed point
- [Inertial navigation device](https://en.wikipedia.org/wiki/Inertial_navigation_system)
	- Computer
	- Motion sensors
		- Accelerometers
	- Rotation sensors
		- Gyroscopes
	- Barometric altimeter
	- Magnetic sensors
		- Magnetometer
- Doesn't account for directional drift through fluid medium
	- Generally doesn't take currents into account
- Speed determined by [pit log](https://en.wikipedia.org/wiki/Pitometer_log), [pitot tube](https://en.wikipedia.org/wiki/Pitot_tube), [pit sword](https://en.wikipedia.org/wiki/Pit_sword)
 
# [Underwater Acoustic Positioning](https://en.wikipedia.org/wiki/Underwater_acoustic_positioning_system)

- Acoustic distance and/or direction measurements
- Long Baseline (LBL)
	- Markers on the sea floor
	- Not relevant
- Ultra-Short-Baseline (USBL)
	- Use beacon at surface vessel
	- Not as accurate
- Short-Baseline (SBL)
	- Multiple transducers at the boat
		- Widen baseline as much as possible
- [GPS Intelligent Buoys (GIB)](https://en.wikipedia.org/wiki/GPS_intelligent_buoys)
	- Inverted long-baseline
	- [Italian Thesis - An Underwater Acoustic Positioning System Based on Buoys with GPS](https://core.ac.uk/download/pdf/14694283.pdf)
- [Dynamic Positioning Committee - ACOUSTIC POSITIONING SYSTEMS “A PRACTICAL OVERVIEW OF CURRENT SYSTEMS”](https://dynamic-positioning.com/proceedings/dp1998/SVickery.PDF)
- [A Study of a Short-Baseline Acoustic Positioning System for Offshore Vessels](https://www.tandfonline.com/doi/pdf/10.1080/014904199273579)
- [Tracking, Navigation, Positioning and Communication Sensors for AUV, ROV, USV](https://www.unmannedsystemstechnology.com/company/sonardyne-international/)
- [Nortek Group - New to subsea navigation?](https://www.nortekgroup.com/knowledge-center/wiki/new-to-subsea-navigation)
 
# Doppler Velocity Log

- [Wiki](https://en.wikipedia.org/wiki/Acoustic_Doppler_current_profiler#DVL)
- Track see floor
   

- Two challenges
	- Global location identification
		- Not typical to AUV, domain specific
	- Maintaining dead reckoning location
 
Communications
 
- Acoustic communications
	- 50 Hz - 50 kHz
	- JANUS
		- STANAG 4748
	- [https://ieeexplore.ieee.org/document/7017134](https://ieeexplore.ieee.org/document/7017134)
- Iridium
	- Radiation for finding when dead?

Kongsberg
 
# [Hugin](https://www.kongsberg.com/maritime/products/marine-robotics/autonomous-underwater-vehicles/AUV-hugin/)
 ![hugin1020x204](../../../../../img/OneNote/AUV%20image%2056195439004b7e63.jpeg)

- 3, 4.5 km depth rated
- Started in the 90s
- Operator-supervised
	- Acoustic tether
	- Semi or fully autonomous
- Aided inertial navigation system
	- AINS
- Sensors
	- Synthetic aperture sonar
		- Or side-scan sonar
	- Multibeam echo sounder
	- Sub-bottom profiler
	- Camera
	- CTD
	- Volume Search sonar
- Lithium polymer battery
	- 24 kWh power packs
	- 100 hrs at 4 knots
- [Product Spec](https://www.kongsberg.com/globalassets/maritime/km-products/product-documents/hugin-product-specification)
- [Paper](https://www.kongsberg.com/globalassets/maritime/km-products/product-documents/hugin-auv-concept-and-operational-experiences-to-date)
- [Hugin Family](https://www.kongsberg.com/globalassets/maritime/km-products/product-documents/hugin-family-of-auvs)
 
# [Hugin Superior](https://www.kongsberg.com/maritime/products/marine-robotics/autonomous-underwater-vehicles/AUV-hugin-superior/)
 ![huginsuperior1020x205](../../../../../img/OneNote/AUV%20image%208a433c2c8f5765cf.jpeg)

- 6 km depth rated
- 62.5 kWh packs
	- 72/52 hrs at 3/4 knots
- [Product Spec](https://www.kongsberg.com/globalassets/maritime/km-products/product-documents/hugin-superior.pdf)

![Superior Navigation Improved insitu navigation and...](../../../../../img/OneNote/AUV%20image%203df336106242cf52.png)  

# [Eelume](https://www.kongsberg.com/maritime/products/marine-robotics/autonomous-underwater-vehicles/AUV-eelume/)
 ![Eelume_Ekstrabilde_U_tekst.jpg](../../../../../img/OneNote/AUV%20image%2032b60600b5053145.jpeg)  

- Modular
- Both ends as two actuators
- 500m depth
- Underwater 24/7
- [Data sheet](https://www.kongsberg.com/globalassets/maritime/km-products/product-documents/eelume----underwater-intervention-vehicle)

Challenges
 
- Navigation
- LARS

[Bluefin Robotics](https://gdmissionsystems.com/underwater-vehicles/bluefin-robotics)
 
# 9

![Inside The Bluefin9 UUV](../../../../../img/OneNote/AUV%20image%20bc98421620bdb077.jpeg)

- 1.9 kWh
	- 8 hrs @ 3 kt
- 70 kg
 
# 12

![General Dynamics Bluefin12 UUV Base Model Diagram](../../../../../img/OneNote/AUV%20image%206e73c9ddcc80e05c.jpeg)

- Medium-class
- 4 x 1.9 kWh
	- 24hr @ 3 kt
	- 36hr @ 2 kt
- 250 kg
 
# 21

- Highly modular
- 13.5 kWh
	- 25 hrs @ 3 kt
	- Lithium Polymer
- 750 kg
- [Case study](https://gdmissionsystems.com/articles/2016/09/16/news-2016-bluefin-uuv-goes-deep-into-the-arctic-at-icex-2016)
 
# HAUV

![Exported image](../../../../../img/OneNote/AUV%20image%200d2a4a5db45b6f15.png)

- Hull inspection
- Port & harbour inspection
- UXO
- 1.5 kWh
	- 3.5 hrs
	- Lithium polymer
- 72 kg

[Teledyne](http://www.teledynemarine.com/gavia/)
 
# Gavia

![Exported image](../../../../../img/OneNote/AUV%20image%202660fea4df34417b.png)  

- 50 - 130 kg
- 500 m or 1 km depth
- [1 - 3] x 1.5 kW
 
# Osprey

![Exported image](../../../../../img/OneNote/AUV%20image%20b5b7b546e68d7904.jpeg)

- Newest
- 400 kg
- 1 km depth
- [1 - 3] x 6.7 kW
 
# SeaRaptor

![Exported image](../../../../../img/OneNote/AUV%20image%20f7ebdde170df954a.png)

- 1 t
- 3 or 6 km depth
- 13 kWh

ISE
 
# [Explorer](https://ise.bc.ca/product/explorer/)

![Exported image](../../../../../img/OneNote/AUV%20image%203b340e78fa9e9064.png)

- [Data sheet](https://ise.bc.ca/wp-content/uploads/2017/12/Explorer_SpecSheet.pdf)
- Applications
	- Survey
	- Inspection
- 3 - 6 km depth
- 620 - 1700 kg
- 18 - 48 kWh
	- 24 - 85 hrs endurance
- Lithium-ion
 
# [Theseus](https://ise.bc.ca/product/theseus-auv/)

![Exported image](../../../../../img/OneNote/AUV%20image%200fb57ae5dd06f499.png)

- [Data sheet](https://ise.bc.ca/wp-content/uploads/2017/12/Theseus-AUV.pdf)
- Lay lengths of fibre optic under arctic ice pack
- 8600 kg
- 1 km depth
- 600 kWh

Atlas Elektronik

# [SeaCat](https://www.atlas-elektronik.com/solutions/unmanned-naval-systems/seacat.html)

![Exported image](../../../../../img/OneNote/AUV%20image%20ba7f6e7f223acf18.jpeg)

- 600m depth
- 130 - 220 kg