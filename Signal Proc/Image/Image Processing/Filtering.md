---
onenote-id: 0-5223391384270af635f883b364c0daf8!1-D084F068F621FF9!3708
---
Noise
 
- Sources
	- Low-level noise
		- Light fluctuations
		- Sensor noise
		- Quantisation effects
		- Finite precision
	- Scene clutter
		- Shadows
		- Extraneous objects
- Assumption for low-level noise
	- Surrounding pixels contain relevant information
	- Average noise can reduce its effect
 
# Salt & Pepper

- Binary noise
	- Electrical interference etc
 ![Exported image](../../../../img/OneNote/Filtering%20image%20046f91ec026c4da5.png)  
![Machine generated alternative text 0200](../../../../img/OneNote/Filtering%20image%20d2b6589afa384c77.png)  

- Use median filter
	- Introduce no new information
 ![Machine generated alternative text 25 SP Noise Aft...](../../../../img/OneNote/Filtering%20image%20eb4a8e4b9ae3d0cc.png)  

- Lots of redundancy

# Additive Noise

- Add noise instead of setting pixel values
- Natural sources of noise well modelled by Gaussian
 ![Exported image](../../../../img/OneNote/Filtering%20image%209aaa1fdfbc0e5f71.png)  
![Machine generated alternative text fx,y Ix,y image...](../../../../img/OneNote/Filtering%20image%20e0a08c2ffb55ecb3.png)  
![100 1000 Central limit theorem Because the Gaussia...](../../../../img/OneNote/Filtering%20image%20a9f572f448dc438d.png)  

- Capture multiple images
	- Average to remove noise
- Use mean filter
	- Lose information
	- Low Pass Filter
 ![Original 15x15 aaaaaaaa aaaaaaaa ...a aaaaaaaa Il ...](../../../../img/OneNote/Filtering%20image%20a3fe8451414af0c9.png)