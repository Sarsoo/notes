- Output of [[Convolutional Layer|conv]], c, layers are added to inputs of [[upconv]], d, layers
- Element-wise, not channel appending
- Propagate high frequency information to later layers
- Two types
	- Additive
		- [[ResNet]]
		- [[Super-resolution]] auto-encoder
- Concatenative
	- Densely connected architectures
	- DenseNet
	- [[FlowNet]]

![[STEM/img/skip-connections.png]]

[AI Summer - Skip Connections](https://theaisummer.com/skip-connections/)
[Arxiv - Visualising the Loss Landscape](https://arxiv.org/abs/1712.09913)