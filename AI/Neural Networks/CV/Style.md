---
onenote-id: 0-a9b38a65a28e05c4124a2b04697c7057!1-D084F068F621FF9!3714
---
[TDS - Neural Networks Intuitions: 2. Dot product, Gram Matrix and Neural Style Transfer](https://towardsdatascience.com/neural-networks-intuitions-2-dot-product-gram-matrix-and-neural-style-transfer-5d39653e7916)  
[Keras - Transfer Learning](https://keras.io/guides/transfer_learning/)

Non-Photorealistic Rendering (NPR)

Content
 
- Appearance-invariant representation of content in late conv layer
	- When trained on general imagery
- Look late in network
- Not layer 5 for some remaining structure
	- Otherwise too abstract
 ![depth64 convl 2 depth con v 2 conv2 128 depth256 c...](../../../../img/OneNote/Style%20image%20bc74b854993dceb8.png)  

Style
 
- Low to mid-level features
 ![de convl 2 nv2 conv2 2 con conv3 conv3 conv3 3 4 d...](../../../../img/OneNote/Style%20image%20a39ca27ed924e4ce.png)

Descriptors
 
- Content
	- $C \left(\right. x \left.\right)$
	- Vectorised activation of conv4_2 layer
		- Or conv5_1
			- More abstract
- Style
	- $S \left(\right. x \left.\right)$
	- Vectorised activations of conv_n__1 layers
	- Gram matrix
		- Covariance matrix
		- Grammian
		- All combinations of dot products
		- $g_{i j} = v_{i}^{T} v_{j}$

$C \left(\right. x \left.\right)$ $S \left(\right. x \left.\right)$ $g_{i j} = v_{i}^{T} v_{j}$

![Given a source image p And an exemplar style image...](../../../../img/OneNote/Style%20image%2033323d8a85549638.png) ![Take p and add Gaussian noise e.g. x p 0.1 VGG 19 ...](../../../../img/OneNote/Style%20image%20aca16da35ae8de16.png)

$L o s s \left(x\right) = \left|C \left(x\right) - C \left(p\right)\right| + k \left|S \left(x\right) - S \left(a\right)\right|$  

- K typically of the order of 10^5 to make Grammian similar

![Compute and Denve Loss Input x init to noisy p X c...](../../../../img/OneNote/Style%20image%20c057a3b72b0fba09.png)

Issues
 
- Takes a long time
	- Use an FCN instead
		- Trained on a per style basis
- Doesn't work well on high frequency sketches
	- Graphite

$k$  

- Different orders of magnitude vary amount of applied style
 ![104 Wassily Kandinsky 100](../../../../img/OneNote/Style%20image%20d34caedc01c44d54.png)

FCN
 
- Symmetric FCN with ResNet backbone
- Learning an image transform
 ![Convolution Deconvolution](../../../../img/OneNote/Style%20image%20cabfc735cd4bd6f2.png)  
$L o s s \left(x\right) = \left|C \left(x\right) - C \left(p\right)\right| + k \left|S \left(x\right) - S \left(a\right)\right| + T V  t e r m$  

- P and a swapped places
- Goes through bottleneck
	- Need TV term
- Needs only a feedforward pass

![Style The Starry Night, Vincent van Gogh, 1889 Sou...](../../../../img/OneNote/Style%20image%206fc067d12654e9f8.png)

Perceptual Loss
 
- Content loss

AM = Activation Maximisation