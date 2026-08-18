- $y$ is 0/1
	- 0 for positive
	- 1 for negative
		- Collapses to 0
- Squared L2 norm
- $m$ is margin
$$L(a,p)=\frac{1}{2}(1-y)\left|f(a)-f(p)\right|^2_2+\frac{1}{2}y\{\max(0,m-|f(a)-f(p)|_2^2\}$$

$$\mathfrak{L}=\frac{1}{2N}\sum^{N}_{i=1}\left[(1-y_i)|f(a_i)-f(p_i)|^2_2+y\{\max(0,m-|f(a_i-f(p_i)|^2_2\}\right]$$

| ![I](../../../../img/OneNote/Visual%20Search%20image%203fc5eaa38b1567cf.png) | ![fa fp La,p](../../../../img/OneNote/Visual%20Search%20image%20991d6b9262844283.png) |
| ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
