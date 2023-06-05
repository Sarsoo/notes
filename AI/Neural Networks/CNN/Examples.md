# LeNet
- 1990's
![lenet-1989](../../../img/lenet-1989.png)
- 1989
![lenet-1998](../../../img/lenet-1998.png)
- 1998

# AlexNet
2012

- [[Activation Functions#ReLu|ReLu]]
- Normalisation

![alexnet](../../../img/alexnet.png)

# VGG
2015

- 16 layers over AlexNet's 8
- Looking at vanishing gradient problem
	- Xavier
- Similar kernel size throughout
- Gradual filter increase

![vgg-spec](../../../img/vgg-spec.png)
![vgg-arch](../../../img/vgg-arch.png)

# GoogLeNet
2015

- [Inception Layer](Inception%20Layer.md)s
- Multiple [[Deep Learning#Loss Function|Loss]] Functions

![googlenet](../../../img/googlenet.png)

## [Inception Layer](Inception%20Layer.md)
![googlenet-inception](../../../img/googlenet-inception.png)
## Auxiliary [[Deep Learning#Loss Function|Loss]] Functions
- Two other SoftMax blocks
- Help train really deep network
	- Vanishing gradient problem

![googlenet-auxilliary-loss](../../../img/googlenet-auxilliary-loss.png)