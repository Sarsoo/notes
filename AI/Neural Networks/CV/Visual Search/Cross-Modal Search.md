- Sketch and images different modes
- Backbone is single branch being used for network
	- InceptionV3
- Partially shared weights between anchor and positive in early stages
	- Low-level features are not same between sketch and photo
	- Needs more complex curriculum
- Use data augmentation for sketches
	- ![Data augmentation](../../../../img/OneNote/Visual%20Search%20image%2034fcdacb03ceb3ea.png)

![anchor Structure net Sketch anchor Softmax loss po...](../../../../img/OneNote/Visual%20Search%20image%2067b935618fee7e80.png)

![Indexing offline Structure network Image Structure...](../../../../img/OneNote/Visual%20Search%20image%207c97cd2fe4f3fc62.png)

# Process
1. Train Unshared Layers
	- Train sketch branch from scratch
	- Fine-tune image branch from pre-trained (ImageNet)
2. Train Shared Layers
	- Form a 2-branch network with pretrained weights
	- Freeze unshared layers
	- Train the shared layers with softmax loss
3. Regression With Triplet Loss
	- Form a triplet network
	- Train the whole network with triplet loss + softmax loss
4. Fine-tune on auxillary sketch-photo dataset (optional)
	- e.g sketchy [Sangkloy et al. 2016]