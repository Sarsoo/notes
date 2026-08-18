---
onenote-id: 0-eb18c26091520cdc057bc505d8b88417!1-D084F068F621FF9!3708
---
![Exported image](../../../../img/OneNote/Scale-Space%20image%20ffe5300dbec03e9f.png)

- Thinking about features that occur at different scales
	- Persistent over different levels of blur

Stack of images blurred at different scales

- Octave intervals
	- Sigma = 1, 2, 4, 8, …
- Low-pass pyramid
	- Or Image Pyramid
- Band-pass pyramid
	- Differences between levels

Can be used to find key points

- Stable
	- Over scale
- Repeatable
	- From different views

![Machine generated alternative text Corners readily...](../../../../img/OneNote/Scale-Space%20image%20c9317f11124d091e.png)

Laplacian of Gaussian
 
- Gives band-pass pyramid
- Use non-maxima suppression over scales to find feature at right level
 ![Machine generated alternative text 03 list of](../../../../img/OneNote/Scale-Space%20image%20fbedaec44b772b34.png)  

![Exported image](../../../../img/OneNote/Scale-Space%20image%205f1cbb824f1a5846.png)

[SIFT](../Features.md)

Typically robust to:
 
- 2x Scaling
- 45 Degree Rotation
- Arbitrary Translation