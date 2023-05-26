# Fully Convolutional
- Remove max-pooling
	- Use strided upconv
- Remove FC layers
	- Hurts convergence in non-classification
- Normalisation tricks
	- Batch normalisation
		- Batches of 0 mean and variance 1
	- Leaky ReLu

# Stages
## Generator, G
- Synthesise 'fake' images
- From noise
## Discriminator, D
- Discriminator is a classifier
	- Is image fake or real

![[gan-arch.png]]
![[gan-arch2.png]]

![[gan-results.png]]

# Training
![[gan-training-discriminator.png]]
![[gan-training-generator.png]]

# Code Vector Math for Control
![[cvmfc.png]]
- Do AM to derive code for an image
![[code-vector-math-for-control-results.png]]