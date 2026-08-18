---
title: GAN
tags:
  - ai
  - ai/media
  - art
---
# Fully [Convolution](../../../../Signal%20Proc/Convolution.md)al
- Remove [Max Pooling](../Max%20Pooling.md)
	- Use strided [UpConv](../UpConv.md)
- Remove [FC](../../MLP/MLP.md) layers
	- Hurts convergence in non-[classification](../../../Classification/Classification.md)
- Normalisation tricks
	- Batch normalisation
		- Batches of 0 mean and variance 1
	- Leaky [ReLu](../../Activation%20Functions.md#ReLu)

# Stages
## Generator, G
- Synthesise 'fake' images
- From noise
## Discriminator, D
- Discriminator is a classifier #ai/classification 
	- Is image fake or real
![Real world images o Generator O Sample Sample Real...](../../../../img/OneNote/GAN%20-%20DONE%20image%20809d1fd973860926.png)

![sigmoid function Discriminator Network Z pzz prior...](../../../../img/OneNote/GAN%20-%20DONE%20image%2093178f46926955f1.png)

![gan-results](../../../../img/gan-results.png)]

# Training
![gan-training-discriminator](../../../../img/gan-training-discriminator.png)
![gan-training-generator](../../../../img/gan-training-generator.png)

# Code Vector Math for Control
![cvmfc](../../../../img/cvmfc.png)
- Do [AM](../Interpretation.md#Activation%20Maximisation) to derive code for an image
![code-vector-math-for-control-results](../../../../img/code-vector-math-for-control-results.png)