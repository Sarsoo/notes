---
title: 'cGAN'
tags:
  - ai
  - media
  - art
---
Conditional [GAN](GAN.md)

- Hard to control with [AM](../Interpretation.md#Activation%20Maximisation)
	- Unconditional [GAN](GAN.md)
- Condition synthesis on a class label
- Concatenate unconditional code with conditioning vector
	- Label
- No longer [unsupervised](../../../Learning.md#Un-Supervised)
	- Everything labelled
		- Fake images and dataset
	- **Requires pairing**

![cgan](../../../../img/cgan.png)
![cgan-example](../../../../img/cgan-example.png)

# Image Conditioning Vector
![icv-pos-neg-examples](../../../../img/icv-pos-neg-examples.png)
![icv-results](../../../../img/icv-results.png)

# Text Encoding
- word2vec

![word2vec](../../../../img/word2vec.png)