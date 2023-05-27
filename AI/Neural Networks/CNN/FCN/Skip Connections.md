- Output of conv, c, layers are added to inputs of upconv, d, layers
- Element-wise, not channel appending
- Propagate high frequency information to later layers
- Two types
	- Additive
		- Resnet
		- Super-resolution auto-encoder
- Concatenative
	- Densely connected architectures
	- DenseNet
	- FlowNet

![[skip-connections.png]]

[AI Summer - Skip Connections](https://theaisummer.com/skip-connections/)
[Arxiv - Visualising the Loss Landscape](https://arxiv.org/abs/1712.09913)aaaaa