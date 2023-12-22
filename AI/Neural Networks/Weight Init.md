---
tags:
  - ai
---
- Randomly
	- Gaussian noise with mean = 0
	- Small network
		- Fixed sigma is fine
			- 0.01
		- E.g. 8 layers
			- AlexNet
	- Too large
		- Wont converge
	- Too small
		- Gradient wont propagate back many layers

## Xavier System
$$\sigma=\frac 1 {n_{in}+n_{out}}$$
or
$$\sigma=\sqrt{2/n}$$
* Where $n=\text{filter size}\times n_{out}$
* And $n_{in}$ and $n_{out}$ refer to number of image channels in and out of the layer