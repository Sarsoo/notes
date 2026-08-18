---
onenote-id: 0-17d9568bb9f601b31c4582346a4aeb30!1-D084F068F621FF9!3708
---
Nearest Neighbour
 
- Round transformed coordinate values to integer for indexing
- No new pixel values
 ![100 100 150 150 200 50 18 150 200](../../../../../img/OneNote/Interpolation%20image%2046b92a12ad62658c.png)  

Bi-Linear
 
- Bi = two directions
	- $x  a n d  y$
- Flatten to  
	then  
    
- _Resample_ image
- Creates new pixel values

$x  a n d  y$

![0.6](../../../../../img/OneNote/Interpolation%20image%20edc531a449c0e04d.png)  
![E is at 6.0,2.8 F is at 7.0,2.8 E colour F colour ...](../../../../../img/OneNote/Interpolation%20image%200f4357a2877ae3ec.png)  
![, 6 6.6,2.8](../../../../../img/OneNote/Interpolation%20image%209665d3ac0ad0cd17.png)

![moqqS!3N 00 OGL OGL 00L OG](../../../../../img/OneNote/Interpolation%20image%20493e3be451bb32a9.png) ![Nearest Neighbour 00 100 Bilinear Interpolation](../../../../../img/OneNote/Interpolation%20image%204ff5f2c67c56f753.png)

Performance Metrics
 
1. Transform
2. Inverse transform
3. Mean Squared Error
 ![ml n 1 MSE](../../../../../img/OneNote/Interpolation%20image%202ff748823506707f.png)

Bi-Cubic
 
- Bi = still  
	and  
    
- Cubic = interpolate through 4 points per  
	and  
    
- Patch instead of neighbouring points
- Over-smooths step edges
 ![6.6 7](../../../../../img/OneNote/Interpolation%20image%208b73f6e50587d9ad.png)  
![Bilinear Interpolation Bicubic Interpolation](../../../../../img/OneNote/Interpolation%20image%202949c9b822bea199.png)  

Gaussian
 
- Even smoother
 ![Exported image](../../../../../img/OneNote/Interpolation%20image%2036b686f2711d6bdd.png)  
![0.02 0.04 0.01 0.12 0.40 6.6,2 0.21 0.03 0.10 0.07](../../../../../img/OneNote/Interpolation%20image%20db0827729a0211b4.png)

![o Nearest Neighbour not really interpolation Bilin...](../../../../../img/OneNote/Interpolation%20image%20f6fabd8c7d4be4dd.png)

Aliasing
 
- Nyquist limit
	- Must sample with at least double the sampling rate of the highest frequency in that signal
- Resampling image
	- Must obey Nyquist
	- Must filter out high frequencies from source image
		- Blur image
 ![100 150 200 250 300 350 400 450 500 100 Without pr...](../../../../../img/OneNote/Interpolation%20image%20e469c4d08f7dc9d7.png)