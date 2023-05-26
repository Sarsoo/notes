# LeNet
- 1990's
![[lenet-1989.png]]
- 1989
![[lenet-1998.png]]
- 1998

# AlexNet
2012

- [[Activation Functions#ReLu|ReLu]]
- Normalisation

![[alexnet.png]]

# VGG
2015

- 16 layers over AlexNet's 8
- Looking at vanishing gradient problem
	- Xavier
- Similar kernel size throughout
- Gradual filter increase

![[vgg-spec.png]]
![[vgg-arch.png]]

# GoogLeNet
2015

- [[Inception Layer]]s
- Multiple Loss Functions

![[googlenet.png]]

## [[Inception Layer]]
![[googlenet-inception.png]]
## Auxiliary Loss Functions
- Two other SoftMax blocks
- Help train really deep network
	- Vanishing gradient problem

![[googlenet-auxilliary-loss.png]]