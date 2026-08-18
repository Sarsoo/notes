---
onenote-id: 0-c72eccdc3f1e035e2361745af141ff66!1-D084F068F621FF9!3708
---
Global Colour Histogram
 
Similar overall colour
 
- Quantize RGB values
	- Count bins
	- Normalise
 $c^{'} = f l o o r \left(\frac{c \cdot q}{256}\right)$

- For R, G, B values
- With q divisions
 $b i n = r^{'} q^{2} + g^{'} q + b^{'}$  

Transformed pixel to bin $ \left[\right. 0 ,  \left(q^{3} - 1\right) \left]\right.$

![iiii, 0 Bin 1 Bin 2 Bin3 Bin4 Bin5 Bin 6 Histogram...](../../../img/OneNote/Visual%20Search%20image%20f505af1c798be5e6.png) ![Exported image](../../../img/OneNote/Visual%20Search%20image%202ce83f0e22b2d175.png)

Edge Orientation Histogram
 
- Blur First?
- Divide into cells
- Differentiate image using [Sobel](Image%20Processing/Image%20Processing.md)
- Histogram edge orientations for each cell
- Concatenate bin values for each cell into descriptor

Semantic Gap
 
- Level 1
	- Similar low-level visual features
	- Texture
	- Colour (Colour Histogram)
- Level 2
	- Similar semantic content
	- Object (Cow)
	- Activity
- Level 3
	- High-level concepts
	- War
	- Comedy
	- News

Precision/Recall
 
# Precision

% of returned relevant
 
# Recall

% of relevant returned
 
# Average Precision

Single figure describing performance
 $a p = \frac{\sum_{n = 1}^{M} P \left(n\right) \cdot r e l \left(n\right)}{r}$  
$P \left(\right. n \left.\right)$

- Precision of top n results

$r e l \left(\right. n \left.\right)$

- (result at n is relevant) → bool → int

$r$

- Number of relevant results

$M$

- Dataset of size M
 
# Mean Average Precision

Average of all average precisions for a query