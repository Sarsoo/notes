---
onenote-id: 0-83553f7ed5c9034d11a2422454c5834b!1-D084F068F621FF9!3708
---
Aperture Problem
 
- Only components of motion vector perpendicular to edge direction are detectable
	- Edge moving up window instead of left to right
		- No change like the Sobel

![The Motion Field assigns a velocity vector to each...](../../../img/OneNote/Motion%20image%207a152dd09fdc143d.png) ![A Moving light The image changes so there is optic...](../../../img/OneNote/Motion%20image%206ea492da4593dfbf.png)

Optical Flow
 
- Ambiguous
	- Is the object or background moving
- All that can be computed from pair of images
- Make assumptions to find reasonable estimate
	- Appearance of the object does not change
 ![Exported image](../../../img/OneNote/Motion%20image%204c12befc8402d9ca.png)  

# Motion Constraint

- Object does not change appearance over time
 ![1, y, t is the centre pixel in a n x n neighbourho...](../../../img/OneNote/Motion%20image%20e147d01b6109c23e.png)  
![01 01 01 high order terms Dt 01 DI DI DI 5x DI y D...](../../../img/OneNote/Motion%20image%2036144c80f1ca0e7f.png)  
![01 DI Ix,ly 01 DI vx, vy DI 1 equation 111 00 0 1 ...](../../../img/OneNote/Motion%20image%20b9ed9e61c71097bb.png)

- $I_{t}$ is the frame difference
 
# Spatial Coherence

- Need another constraint to get other unknown
- Assume neighbouring pixels have similar OF
	- Minimal variation in small area
 ![Exported image](../../../img/OneNote/Motion%20image%20b5f8c59f5d20392b.png)

# Three Equations

- Three terms to solve with
 ![vy O](../../../img/OneNote/Motion%20image%20f1c5668570d259cf.png)  
![2 x y Y t](../../../img/OneNote/Motion%20image%2038fa986e20fe7149.png)  
![21 21 2 ay t ax ay t vy](../../../img/OneNote/Motion%20image%20f9fab7886db4bb56.png)  
![01 01 ay 1A U Iterative solution Estimate vx and v...](../../../img/OneNote/Motion%20image%20f80a48701d025753.png)  
![Gradients dldy abef dldt efgh aCeg Cdgh a d x h u ...](../../../img/OneNote/Motion%20image%20e2673ebbba1aec91.png)

Shot Detection
 
- HSV colour space
 ![HUNG PARLIAMENT Statement expected in Downing Stre...](../../../img/OneNote/Motion%20image%207f444a7509792225.png)  
![Exported image](../../../img/OneNote/Motion%20image%2048cd9b4a4694c5ab.png)

Activity Recognition
 
- Motion history image
	- MHI
- SSD between test and train MHI
 ![T if DU, y, t max O, y, t 1 1 ot erwise](../../../img/OneNote/Motion%20image%203c8a753385b9b499.png)  
![Exported image](../../../img/OneNote/Motion%20image%20ea30d2bf53d8a845.png)

Spatio-Temporal Volume
 ![Spacetime regions x Time t Spacetime rep. of a sho...](../../../img/OneNote/Motion%20image%20b352686e0eb04de0.png)  

- Descriptor
	- Use HOG/SIFT extension
 ![Histogram of oriented spatial Histogram of optical...](../../../img/OneNote/Motion%20image%20c244b750d3671697.png)  

# Space-Time Patches

![Clustering cl Classification](../../../img/OneNote/Motion%20image%20af7d464b33af7e92.png)  

# Bag of Video Words

![spacetime patches Extraction of Local features Occ...](../../../img/OneNote/Motion%20image%201afcf03a81ddec22.png)

Two Stream Network
 
- Not Siamese
- Not deeply calculating optical flow
- Both initialised with ImageNet weights
- Averaging gave good score
	- 86.9% mAP
 ![ense Max pooling Video Stride Convl 3 Stride tl Co...](../../../img/OneNote/Motion%20image%20639b7d30f0f25023.png)  

[FlowNet](../../../../AI/Neural%20Networks/CNN/FCN/FCN.md)
