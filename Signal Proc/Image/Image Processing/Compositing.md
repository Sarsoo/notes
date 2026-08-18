---
onenote-id: 0-432b0ea808750aa11760094cff1bde48!1-D084F068F621FF9!3708
---
_Process of combining visual elements from multiple images into a single image_

Matte
 ![A Matte is used to define area of interest](../../../../img/OneNote/Compositing%20image%20336b51cbbee216c9.png)  

- Effectively a mask
- Doesn't have to be binary
- Encode in alpha channel

Porter-Duff
 
- 12 permutations to combine images
 ![Both Source Dest Atop DestAtop Xor Over Dest Over ...](../../../../img/OneNote/Compositing%20image%2010c4a60187eb7f47.png)

- Alpha is 1
 ![A src . S Adest Aboth Atop Out Dest DestAtop De st...](../../../../img/OneNote/Compositing%20image%20473c8e3fcef4309a.png)

- Both is intersection
- 0 will enforce transparent hole
 
# Alpha Blending

- Consider area of contribution within each pixel

![A in a Opaque A and B Partially transparent A and ...](../../../../img/OneNote/Compositing%20image%201701a18a7e8404b1.png)  
![Transparency of B dest interpreted as an area Tran...](../../../../img/OneNote/Compositing%20image%20d8cf5ad36148ab6e.png)  

# Problems

- Hard to get a good matte
	- Thin stuff like hair

![Exported image](../../../../img/OneNote/Compositing%20image%20c98f2f956a24f0f7.png)

Gradient Domain Compositing
 
- Retain all edge (gradient) information at boundary
- Use Laplacian
	- Instead of  
		, use  
        
	- $L$ is the Laplacian calculated from the source image
	- $K$ are destination, $L$ source
- Independent for each colour channel

![1 o 1 0 . 1 41 100 Row for each unknown pixel 0 0 ...](../../../../img/OneNote/Compositing%20image%20a6062b10eab670d5.png)

Seam Carving
 
- Content-aware scaling
- Discards non-salient areas to reduce size
 ![Original Scaling warp Seam Carving Reduced size im...](../../../../img/OneNote/Compositing%20image%20fc3ee59b04ce66e8.png)  

- Cut boring sky and grass to make square
	- Don’t change aspect ratio of person or castle
- Each pixel assigned a weight for importance
	- E.g. edge strength
 ![Good seams to drop Bad seam to drop](../../../../img/OneNote/Compositing%20image%205bc236f2476bce77.png)

- High seam
	- Intersects lots of information
- Low seam
	- Boring
 
# Finding

- Consider rows of pixels
	- Seams vertical
- Pick from 3 neighbours with smallest weight
	- Construct smallest weighted seams
 ![Exported image](../../../../img/OneNote/Compositing%20image%20164c19e77bc44172.png)  
![Top row of pixels 2nd row of pixels 3 85 42 5](../../../../img/OneNote/Compositing%20image%20509125aebe04c2dd.png)  
![Top row of pixels 2nd row of pixels 3rd row of pix...](../../../../img/OneNote/Compositing%20image%20cd319ef1f0d49c30.png)  
![Exported image](../../../../img/OneNote/Compositing%20image%206461e33b2b11dba4.png)  

![Exported image](../../../../img/OneNote/Compositing%20image%20e5ac12c6fc2e221e.png)