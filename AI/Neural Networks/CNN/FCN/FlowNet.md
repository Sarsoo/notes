---
title: FlowNet
tags:
  - ai
  - ai/media
---
Optical Flow

- 2-Channel optical flow
	- $dx,dy$
- Two consecutive frames
	- 6-channel [tensor](../../../../Maths/Tensor.md)

![flownet](../../../../img/flownet.png)

# [Skip Connections](Skip%20Connections.md)
- Further through the network information is condensed
	- Less high frequency information
- Link encoder layers to [UpConv](../UpConv.md) layers
	- Append activation maps from encoder to decoder

# Encode
![flownet-encode](../../../../img/flownet-encode.png)

# [UpConv](../UpConv.md)
![flownet-upconv](../../../../img/flownet-upconv.png)

# Training
- Synthetic rendered objects
- Real background images

![flownet-training](../../../../img/flownet-training.png)