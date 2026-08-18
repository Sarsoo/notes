---
onenote-id: 0-0f7b57476ab1017a1cc82781598f3ff4!1-D084F068F621FF9!3714
---
- Pick a dataset
- Pick some networks

- Net structures
	- Number of conv layers
		- Early layers
			- Conv1.5
				- 40x40
				- 4x4 kernel
			- Remove conv1
		- Later layers
			- Conv3.5
				- 13x13
				- 3x3 kernel
				- 100/384 filters
			- Remove conv4
	- Number of dense layers
		- FC3
		- 2000 Nodes
		- Remove FC2
	- Nonlinearity
		- Percentage of ReLu
		- Early conv layers
			- 2
		- Later conv layers
			- 4/5
	- Layer parameters
		- Kernel size
		- Stride
	- Optimisers
		- SGD
		- Adam?
- Parameters
	- Learning rate
		- Constant
			- 1e-1
			- 1e-6
		- Function of epochs
			- Best from above
			- Step down
			- Exponential
			- Sigmoid
	- Momentum?
	- Epochs
		- 50
		- 100
		- 200
- Dataset
	- Splits
		- TR/V/TE
		- 90/9/1
		- 90/5/5
		- 80/10/10
		- 70/15/15
		- 50/25/25
		- 50/5/45
	- Pre-processing
		- Augmentation
		- Mean shifting

[DIGITS TensorFlow](https://github.com/NVIDIA/DIGITS/blob/master/docs/GettingStartedTensorflow.md/#selecting-tensorflow-when-creating-a-model-in-digits)  
[DIGITS Docs](https://docs.nvidia.com/deeplearning/digits/index.html)
 
[Caffe Tutorial](https://caffe.berkeleyvision.org/tutorial/)

Datasets
 
- CIFAR
	- 10
		- 60k images
		- 32x32
		- 10 classes
	- 100
		- 100 classes
			- 600 images each
		- 20 super-classes
- STL10
	- Unsupervised
- [ImageNet](http://image-net.org)
	- ILSVRC
		- ImageNet Large Scale Visual Recognition Challenge
		- 1000 classes
		- 1.3M images
- Lego Bricks
	- [Kaggle](https://www.kaggle.com/joosthazelzet/lego-brick-images)
	- Grey?
	- 16 classes
- [Stanford cars](http://ai.stanford.edu/~jkrause/cars/car_dataset.html)
	- 16k images
	- 196 classes
		- 80 per class?
- [Stanford dogs](http://vision.stanford.edu/aditya86/ImageNetDogs/)
	- 20k images
	- 120 classes

Questions
 
- What if the dataset images don’t match the standard architectures
	- Resize images
	- Modify layer dimensions
		- Leave filter sizes, change stride?

CIFAR-100 Classes
 
|   |   |
|---|---|
|**Superclass**|**Classes**|
|aquatic mammals|beaver, dolphin, otter, seal, whale|
|fish|aquarium fish, flatfish, ray, shark, trout|
|flowers|orchids, poppies, roses, sunflowers, tulips|
|food containers|bottles, bowls, cans, cups, plates|
|fruit and vegetables|apples, mushrooms, oranges, pears, sweet peppers|
|household electrical devices|clock, computer keyboard, lamp, telephone, television|
|household furniture|bed, chair, couch, table, wardrobe|
|insects|bee, beetle, butterfly, caterpillar, cockroach|
|large carnivores|bear, leopard, lion, tiger, wolf|
|large man-made outdoor things|bridge, castle, house, road, skyscraper|
|large natural outdoor scenes|cloud, forest, mountain, plain, sea|
|large omnivores and herbivores|camel, cattle, chimpanzee, elephant, kangaroo|
|medium-sized mammals|fox, porcupine, possum, raccoon, skunk|
|non-insect invertebrates|crab, lobster, snail, spider, worm|
|people|baby, boy, girl, man, woman|
|reptiles|crocodile, dinosaur, lizard, snake, turtle|
|small mammals|hamster, mouse, rabbit, shrew, squirrel|
|trees|maple, oak, palm, pine, willow|
|vehicles 1|bicycle, bus, motorcycle, pickup truck, train|
|vehicles 2|lawn-mower, rocket, streetcar, tank, tractor|
 
1. Dataset splits
2. Parameters
3. Net structures

![,](../../img/OneNote/Image%20CW%20image%2088d40ce883e780d6.png)  

[LearnOpenCV-AlexNet](https://learnopencv.com/understanding-alexnet/)

|   |   |   |   |   |
|---|---|---|---|---|
|**Layer Name**|**Tensor Size**|**Weights**|**Biases**|**Parameters**|
|Input Image|227x227x3|0|0|0|
|Conv-1|55x55x96|34,848|96|34,944|
|MaxPool-1|27x27x96|0|0|0|
|Conv-2|27x27x256|614,400|256|614,656|
|MaxPool-2|13x13x256|0|0|0|
|Conv-3|13x13x384|884,736|384|885,120|
|Conv-4|13x13x384|1,327,104|384|1,327,488|
|Conv-5|13x13x256|884,736|256|884,992|
|MaxPool-3|6x6x256|0|0|0|
|FC-1|4096×1|37,748,736|4,096|37,752,832|
|FC-2|4096×1|16,777,216|4,096|16,781,312|
|FC-3|1000×1|4,096,000|1,000|4,097,000|
|Output|1000×1|0|0|0|
|**Total**||||**62,378,344**|
 
[AlexNet Calcs](https://learnopencv.com/number-of-parameters-and-tensor-sizes-in-convolutional-neural-network/)
 
[nanonets - Data Augmentation](https://nanonets.com/blog/data-augmentation-how-to-use-deep-learning-when-you-have-limited-data-part-2/)