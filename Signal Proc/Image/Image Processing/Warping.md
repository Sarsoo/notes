---
onenote-id: 0-1a00f04be5e40a342e24696973656014!1-D084F068F621FF9!3708
---
Forward Mapping
 
- Map original image onto result
- Pixels only have integer values
- Missing information
	- Holes
 ![50 100 Holes! 50 100 150 200 2 300 200 300 500](../../../../img/OneNote/Warping%20image%20c8a6f505569836c4.png)  

Backward Mapping
 
- Map result pixels onto original
	- Inverse transformation
- All pixels will have a friend
 ![100 150 200 250 400 450 50 100 150 200 250 300 350...](../../../../img/OneNote/Warping%20image%201669cb578ee5a513.png)  

_Digital transformation of a source image into a target image, under some mathematical function defined between the two images_

Boundaries
 
# Negative Coordinates

![Need to shift down by minimum y coordinate from co...](../../../../img/OneNote/Warping%20image%20feaf948696833dd9.png)  
$T_{x} = - m i n ⁡ \left(x\right)$ $T_{y} = - m i n ⁡ \left(y\right)$ $M^{'} = \begin{bmatrix} 1 & 0 & T_{x} \\ 0 & 1 & T_{y} \\ 0 & 0 & 1 \end{bmatrix} M$  
![Exported image](../../../../img/OneNote/Warping%20image%2078ebb3503d8bb252.png)  

# Out of Bounds

$W^{'} = m a x ⁡ \left(x\right) - m i n ⁡ \left(x\right) + 1$ $H^{'} = m a x ⁡ \left(y\right) - m i n ⁡ \left(y\right) + 1$  
![100 R 700 18 200 300 400 500 600 700](../../../../img/OneNote/Warping%20image%20d9066fd1df704121.png)  

Non-Invertable  
 
- Will need to forward map and deal with holes
	- Can’t backward map
 ![Target Ima Source Image](../../../../img/OneNote/Warping%20image%20a11165bf1dd4ee10.png)  

- Treat pixel as quad
	- Area of overlap computed
	- Weighted average of source colour added to image
 
# Fant's Algorithm

- 2-pass approach
- Warp only  
	first
 ![x,y x,y Source Image I termediate Image Pass 1 Pas...](../../../../img/OneNote/Warping%20image%20c1f8d409ad4435e1.png)