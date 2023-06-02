Optical Flow

- 2-Channel optical flow
	- $dx,dy$
- Two consecutive frames
	- 6-channel [tensor](../../../../Maths/Tensor.md)

![flownet](../../../../img/flownet.png)

# [[Skip Connections]]
- Further through the network information is condensed
	- Less high frequency information
- Link encoder layers to [[upconv]] layers
	- Append activation maps from encoder to decoder

# Encode
![flownet-encode](../../../../img/flownet-encode.png)

# [[Upconv]]
![flownet-upconv](../../../../img/flownet-upconv.png)

# Training
- Synthetic rendered objects
- Real background images

![flownet-training](../../../../img/flownet-training.png)