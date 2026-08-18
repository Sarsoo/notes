---
onenote-id: 0-8672986a293c0132198c7f30b3d3afbd!1-D084F068F621FF9!3708
---
Negative Image
 ![Exported image](../../../../img/OneNote/Enhancement%20image%20e922a1b21b36f842.png)  
$g \left(x , y\right) = 1 - f \left(x , y\right)$  

- Assuming normalised greyscale
- No new information
- PDF of intensity values
	- Negative mirrors

Thresholding
 
- Part of segmentation
 $g \left(x , y\right) = \left{\begin{matrix} 1 ,   i f  f \left(x , y\right) > T \\ 0 ,   i f  f \left(\right. x , y \left.\right) \leq T \end{matrix}\right$  
![Exported image](../../../../img/OneNote/Enhancement%20image%20e4ca76c295bf0afc.png)  

- Shift peaks to either side, binary on  
	axis
- Only works for bi-modal distribution
 ![Pixel Count Pixcl Count Pixcl Intensity Pixel Coun...](../../../../img/OneNote/Enhancement%20image%200975135c7ac91daa.png)  

# Optimal Global Thresholding

- K-means with k = 2
- Otsu's method
	- Minimise spread of the peaks
	- _Within class variance_
	- ![Machine generated alternative text aWithinT](../../../../img/OneNote/Enhancement%20image%204490ce20efe22009.png)
      
	- ![nBT noT aT T1 IVI Pi the variance ofthe pixels in ...](../../../../img/OneNote/Enhancement%20image%207a8998eccab42629.png)
		- Expensive
			- Calculates variance
		- Use inter-class variance instead
			- ![J](../../../../img/OneNote/Enhancement%20image%204e17b2641a6228f0.png)
			- ![2 Between](../../../../img/OneNote/Enhancement%20image%206adc9ebfcc238c79.png)
   

# Adaptive Thresholding

- Take non-overlapping windows
	- Calculate average value per window
	- Define threshold relative to mu
 
|   |   |
|---|---|
|![Exported image](../../../../img/OneNote/Enhancement%20image%20c380c52c787d8744.png)|![Exported image](../../../../img/OneNote/Enhancement%20image%202518a5ee91863fdf.png)|
 ![Global T Adaptive T](../../../../img/OneNote/Enhancement%20image%20afa0b9dea8508484.png)  
![Sonnet for Lena Original Global T Sonncl.for,LOita...](../../../../img/OneNote/Enhancement%20image%2088163d547639d84b.png)

Brightness Manipulation
 $g \left(x , y\right) = f \left(x , y\right) + C$  

- Add constant to pixel intensities
- Shift dynamic range
 ![Exported image](../../../../img/OneNote/Enhancement%20image%2093b4910e7ce040e3.png)  
![Brightness Enhanced](../../../../img/OneNote/Enhancement%20image%20a1fe99f6aa08a74d.png)  

Contrast Manipulation
 
- Increase/stretch dynamic range
	- Width of histogram dataset
	- Stretch histogram
		- Clearer perception of histogram differences
 ![Exported image](../../../../img/OneNote/Enhancement%20image%2095764b1ba870a393.png)  
$P_{o u t} = \left(P_{o u t} - c\right) \left(\frac{b - a}{d - c}\right) + a$  

- Upper and lower limit  
	and  
	- Define new dynamic range
- Lowest and highest pixel values in the image,  
	and  
	- $- c$ to begin with in order to scale, $+ a$ at the end
- Scale between two pairs
 ![Contrast Enhanced](../../../../img/OneNote/Enhancement%20image%20b771df0c500118cc.png)  
![Pixel value histogram laae output Pixel intensity ...](../../../../img/OneNote/Enhancement%20image%208b4bb742fe351350.png)

Histogram Equalisation
 
- Reshape PDF
	- Via cumulative
- Make cumulative PDF linear
- Not necessarily good for CV
	- Change semantic meaning of images which may or may not look better
- Monotonic increasing transfer function
 ![Cumulative pdf Linear](../../../../img/OneNote/Enhancement%20image%204cfafd472fcd3286.png)  
![output tnpu](../../../../img/OneNote/Enhancement%20image%201076c22b0562d45c.png)  

- Given pixel of intensity  
	from range  
	- e.g. $L = 256$
 $p_{n} = \frac{n u m b e r  o f  p i x e l s  w i t h  i n t e n s i t y ,  n}{t o t a l  n u m b e r  o f  p i x e l s}$ $T \left(k\right) = f l o o r \left(\left(L - 1\right) \sum_{n = 0}^{k} p_{n}\right)$  
![Original Contrast Enhanced Histogram Equalised Pix...](../../../../img/OneNote/Enhancement%20image%203ad93b4638f8aa5c.png)

Mean-Variance Normalisation
 
- Non-overlapping windows
- Local corrections
- Subtract mean, divide by variance
 ![3](../../../../img/OneNote/Enhancement%20image%207f87295d61735ad0.png)  
![E. refers to mean in a window. V. refers to varian...](../../../../img/OneNote/Enhancement%20image%203cbb1cbde7fde835.png)