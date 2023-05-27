# Activation Maximisation
- Synthesise an ideal image for a class
	- Maximise 1-hot output
	- Maximise [[Activation Functions#SoftMax|SoftMax]]

![[am.png]]
- **Use trained network**
	- Don't update weights
- [[Architectures|Feedforward]] noise
	- [[Back-Propagation|Back-propagate]] [[Deep Learning#Loss Function|loss]]
		- Don't update weights
		- Update image

![[am-process.png]]
## Regulariser
- Fit to natural image statistics
- Prone to high frequency noise
	- Minimise
- Total variation
	- $x^*$ is the best solution to minimise [[Deep Learning#Loss Function|loss]]

$$x^*=\text{argmin}_{x\in \mathbb R^{H\times W\times C}}\mathcal l(\phi(x),\phi_0)$$
- Won't work
$$x^*=\text{argmin}_{x\in \mathbb R^{H\times W\times C}}\mathcal l(\phi(x),\phi_0)+\lambda\mathcal R(x)$$
- Need a regulariser like above

![[am-regulariser.png]]

$$\mathcal R_{V^\beta}(f)=\int_\Omega\left(\left(\frac{\partial f}{\partial u}(u,v)\right)^2+\left(\frac{\partial f}{\partial v}(u,v)\right)^2\right)^{\frac \beta 2}du\space dv$$

$$\mathcal R_{V^\beta}(x)=\sum_{i,j}\left(\left(x_{i,j+1}-x_{ij}\right)^2+\left(x_{i+1,j}-x_{ij}\right)^2\right)^{\frac \beta 2}$$
- Beta
	- Degree of smoothing