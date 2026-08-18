---
onenote-id: 0-96fb900ce3ec4a34936840345bec0074!1-D084F068F621FF9!3708
---
Blur
 
# Box Filter
 $1/9 \begin{bmatrix} 1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1 \end{bmatrix}$  
![Exported image](../../../../img/OneNote/Image%20Processing%20image%2095fbf13cce30a631.png)  

# Gaussian
 
Smoother blend

$G_{𝜎} = \frac{1}{2 \pi 𝜎^{2}} e^{- \frac{\left(x^{2} + y^{2}\right)}{\left(2 𝜎\right)^{2}}}$  
$\begin{bmatrix} 0 . 06 & 0 . 13 & 0 . 06 \\ 0 . 13 & 0 . 24 & 0 . 13 \\ 0 . 06 & 0 . 13 & 0 . 06 \end{bmatrix}$  
![Exported image](../../../../img/OneNote/Image%20Processing%20image%204a78b4503b116f9a.png)

![Exported image](../../../../img/OneNote/Image%20Processing%20image%2013baf587a8d15b78.png)

Convolution
 $G \left[i ,   j\right] = H \left[u ,   v\right] * F \left[i ,   j\right]$ $G \left[i ,   j\right] = \sum_{u = - k}^{k} \sum_{v = - k}^{k} H \left[u ,   v\right] F \left[i - u ,   j - v\right]$  

- If filter kernel is not isotropic then technically it's just cross-correlation
- Because i/j minus u/v
	- Kernel is flipped vertically and horizontally when multiplying
	- Cross-correlation is not flipped
	- By convention we don't flip kernel
 
# Convolution Theorem

![Care Fl. indicates FT of function. fx,y mage hx,y ...](../../../../img/OneNote/Image%20Processing%20image%2065bb8f74f56a3589.png)   
# Padding

- Can't include edge pixels
	- Include extra border pixels
	- e.g. 0 padding
 
# Striding

- Axis incrementing value
	- Slide over all pixels
		- Stride of 1

Edge Detection
 $\nabla f = \left[\frac{𝜕 f}{𝜕 x} , \frac{𝜕 f}{𝜕 y}\right]$

- Partial derivative of image in both axes
- 2D, plot points in direction of most rapid increase in intensity
- Blur then edge detect to remove noise in derivative
 
## Edge Strength

$\left‖\nabla f\right‖ = \sqrt{\frac{𝜕 f}{𝜕 x}^{2} + \frac{𝜕 f}{𝜕 y}^{2}}$  

## Edge Direction

$𝜃 = \left(t a n\right)^{- 1} ⁡ \left(\left(\frac{𝜕 f}{𝜕 y}\right)/\left(\frac{𝜕 f}{𝜕 x}\right)\right)$  

# Sobel
 $\frac{𝜕 f}{𝜕 x} = \begin{bmatrix} 1 & 0 & - 1 \\ 2 & 0 & - 2 \\ 1 & 0 & - 1 \end{bmatrix}$  
$\frac{𝜕 f}{𝜕 y} = \begin{bmatrix} 1 & 2 & 1 \\ 0 & 0 & 0 \\ - 1 & - 2 & - 1 \end{bmatrix}$  

- Gaussian derivative differentiates in one axis and smooths in the orthogonal one
- Problems
	- Imprecisely localised
	- Wide magnitude range of edges should be collected
	- Gradient magnitude differs and different scales
		- Which one is relevant
		- Compare across scales
			- Persistent edges are salient
	- Thick edges
		- Non-max suppression
	- How to link edge points into curves
		- Hysteresis thresholding

2D DFT
 $F \left(u ,   v\right) = \frac{1}{M N} \sum_{x = 0}^{M - 1} \sum_{y = 0}^{N - 1} f \left(x , y\right) \cdot e^{- 2 \pi i \left(\frac{u x}{M} + \frac{v y}{N}\right)}$  
$f \left(x ,   y\right) = \sum_{u = 0}^{M - 1} \sum_{v = 0}^{N - 1} F \left(u , v\right) \cdot e^{2 \pi i \left(\frac{u x}{M} + \frac{v y}{N}\right)}$

Sharpening
 $G = F + 𝛼 \left(F - F * H\right)$  
$𝛼 \begin{bmatrix} \begin{bmatrix} 0 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0 \end{bmatrix} - 1/9 \begin{bmatrix} 1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1 \end{bmatrix} \end{bmatrix}$  
![scaled impulse Gaussian Laplacian of Gaussian](../../../../img/OneNote/Image%20Processing%20image%202f5649ab47f39aca.png)

Smoothed Edge Detection
 
- Convolution is associative
	- Combine filters
 
# Derivative of gaussian
 ![Exported image](../../../../img/OneNote/Image%20Processing%20image%201548b56527b2517e.png)

Ripples cause grid

Smooth

LOW PASS

HIGH PASS

![We can compute the FT of a 2D signal i.e. an image...](../../../../img/OneNote/Image%20Processing%20image%204a1239af5d40db4e.png)

_Isotropic_  
Rotationally symmetrical

![Exported image](../../../../img/OneNote/Image%20Processing%20image%20bd2e668658e112d9.png)

- Derivative of image

Second Derivative

![Machine generated alternative text 2nd order Numer...](../../../../img/OneNote/Image%20Processing%20image%205644f27ed3c3bb40.png)  
![Machine generated alternative text 00 1st derivati...](../../../../img/OneNote/Image%20Processing%20image%20f431f44bbbd800ec.png)  

- Zero crossings are locations of edges
	- maxima
 
# Laplacian

$\nabla^{2} f = \frac{𝜕^{2} f}{𝜕 x^{2}} + \frac{𝜕^{2} f}{𝜕 y^{2}}$

- Image sharpening
 $\begin{bmatrix} 0 & - 1 & 0 \\ - 1 & x & - 1 \\ 0 & - 1 & 0 \end{bmatrix}$  

- Where  
	is the level of sharpening
 ![Machine generated alternative text in ID in 2D Mex...](../../../../img/OneNote/Image%20Processing%20image%20a63133da4a0a87af.png)  

Edge Scale
 
- Strong edges persist longer as you blur
- Structural edges persist across scale
	- Physical boundaries
	- Shadow and noise tend not to
 ![3x3 window 7x7 window 15x15 window](../../../../img/OneNote/Image%20Processing%20image%20d545120c5fbc0bb9.png)

Non-Maxima Suppression
 ![Pixel intensity Xl If fx fxl fx fX1 x](../../../../img/OneNote/Image%20Processing%20image%200c62109d6f6d23ca.png)

- Find just the turning point
	- 0 everything else

Canny

- Turn non-binary Sobel edges into binary edges
 
# NMS

- Perform non-maxima suppression in direction of max gradient
 ![gx,y magnitude orientation Gradient magnitude gx,y...](../../../../img/OneNote/Image%20Processing%20image%20c48376779f19f1f7.png)  

# Edge Labelling

- After NMS
- To join points into contours
 ![Machine generated alternative text x gradient edge...](../../../../img/OneNote/Image%20Processing%20image%20c13136067bcc8f61.png)  

# Hysteresis

- How to class different strengths of edges
- Above high threshold
	- Strong edge
- Below low threshold
	- Strong not edge
- In-between
	- Edge only if connected to other edges
 ![Exported image](../../../../img/OneNote/Image%20Processing%20image%20fc1d41d777357828.png)  

![Machine generated alternative text fine scale high...](../../../../img/OneNote/Image%20Processing%20image%207b1d15991336a2b9.png)

