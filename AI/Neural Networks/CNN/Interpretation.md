# Activation Maximisation
- Synthesise an ideal image for a class
	- Maximise 1-hot output
	- Maximise [[Activation Functions#SoftMax|SoftMax]]

![[am.png]]
- **Use trained network**
	- Don't update weights
- Feedforward noise
	- [[Back-Propagation|Back-propagate]] loss
		- Don't update weights
		- Update image

![[am-process.png]]
## Regulariser
- Fit to natural image statistics
- Prone to high frequency noise
	- Minimise
- Total variation
	- $x^*$ is the best solution to minimise loss