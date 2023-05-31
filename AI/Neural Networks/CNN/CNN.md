## Before 2010s
- Data hungry
	- Need lots of training data
- Processing power
- Niche
	- No-one cared/knew about CNNs
## After
- [ImageNet](../CV/Datasets.md#ImageNet)
	- 16m images, 1000 classes
- GPUs
	- General processing GPUs
	- CUDA
- NIPS/ECCV 2012
	- Double digit % gain on [ImageNet](../CV/Datasets.md#ImageNet) accuracy

# Full Connected
[[MLP|Dense]]
- Move from [[Convolutional Layer|convolutional]] operations towards vector output
- Stochastic drop-out
	- Sub-sample channels and only connect some to [[MLP|dense]] layers

# As a Descriptor
- Most powerful as a deeply learned feature extractor
- [[MLP|Dense]] classifier at the end isn't fantastic
	- Use SVM to classify prior to penultimate layer

![[cnn-descriptor.png]]

# Finetuning
- Observations
	- Most CNNs have similar weights in [[Convolutional Layer|conv1]]
	- Most useful CNNs have several [[Convolutional Layer|conv layers]]
		- Many weights
		- Lots of training data
	- Training data is hard to get
		- Labelling
- Reuse weights from other network
- Freeze weights in first 3-5 [[Convolutional Layer|conv layers]]
	- Learning rate = 0
	- Randomly initialise remaining layers
	- Continue with existing weights

![[fine-tuning-freezing.png]]
# Training
- Validation & training [[Deep Learning#Loss Function|loss]]
- Early
	- Under-fitting
	- Training not representative
- Later
	- Overfitting
- V.[[Deep Learning#Loss Function|loss]] can help adjust learning rate
	- Or indicate when to stop training

![[under-over-fitting.png]]