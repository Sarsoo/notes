Fully [[Convolution]]al Network

Convolutional and up-convolutional layers with [[Activation Functions#ReLu|ReLu]] but no others (pooling)
- All some sort of Encoder-Decoder

Contractive → [[UpConv]]

# Image Sementation
- For visual output
	- Previously image $\rightarrow$ vector
- Additional layers to up-sample representation to an image
	- Up-[[convolution]]al
	- De-[[convolution]]al

![[fcn-uses.png]]

![[fcn-arch.png]]

# Training
- Rarely from scratch
- Pre-trained weights
- Replace final layers
	- FC layers
	- White-noise initialised
- Add [[upconv]] layer(s)
	- Fine-tune train
	- Freeze others
	- Annotated GT images
- Can use summed per-pixel log loss

# Evaluation
![[fcn-eval.png]]
- SDS
	- Classical method
	- 52% mAP
- FCN
	- 62% mAP
- Intersection over Union
	- IOU
	- Jaccard
	- Averaged over all images
	- $J(A,B)=\frac{|A\cap B|}{|A\cup B|}$