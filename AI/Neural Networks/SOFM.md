---
onenote-id: 0-9be7670744bc0d0d3beb1f65dd83e6ae!1-D084F068F621FF9!3714
---
Kohonen Feature Map
 
- Spatial location of output neural corresponds to feature of input data
	- Higher-D feature map
- Vector coding
- Unsupervised
	- Competitive learning
		- Only one neuron fires at once
		- Use negative feedback to inhibit others
		- Hebbian
- Maintains topology
	- Forms a topographic map of input patterns
		- Spatial locations of neurons in lattice are indicative of intrinsic statistical features of training patterns
		- Similar to brain
	- _The spatial location of an output neuron in a topographic map corresponds to a particular domain or feature of data drawn from the input space_
- Inherently nonlinear
	- Nonlinear generalisation of PCA
- Capable of data compression
	- Dimensionality reduction of input
 ![o o o 2Dim](../../../img/OneNote/SOFM%20image%20d8e7b2185a6cfa5c.png)  
![Input vector Layer of source nodes Each neuron has...](../../../img/OneNote/SOFM%20image%20d6b1f918dd83227f.png)  

SOFM
 ![1. 2. 3. 1. 2. Initialisation random values for in...](../../../img/OneNote/SOFM%20image%2007f6806ca0df7fc6.png)

Density Matching
 
- Make weights look like inputs
- Reflect variations in stats of input distribution
- High probability vectors map to larger regions than low probability vectors
- Tends to over-represent low prob. regions and vice versa
	- Use Gaussian neighbourhood function instead of rectangle
 ![Gaussian Function exp djJ2 where diJ2 denotes late...](../../../img/OneNote/SOFM%20image%20c61dc5f888d876a2.png)  

Continuous → Discrete Space
 
- Discrete space is node lattice
- Map from continuous input space to discrete space
- Application-specific output could be
	- Index of winning neuron
		- Position
	- Closest weight vector
		- Neuron
- Vector Quantisation
	- Vector coding
	- Compression
- Synaptic weight vector of winner can be viewed as pointer into input space
	- Coordinates of image of neuron projected in input space
 ![To begin with, let denote a spatially continuous i...](../../../img/OneNote/SOFM%20image%20ada012a88ada5450.png)  
![Feature map Cts Discrete output space Continuous i...](../../../img/OneNote/SOFM%20image%20cfff3365a9690fbe.png)  

![Example uniformly distributed 2dim input, 5 x 5 ne...](../../../img/OneNote/SOFM%20image%2008e9ed5fb3e3c88d.png) ![Twodimensional array of postsynaptic neurons Bundl...](../../../img/OneNote/SOFM%20image%203d03650bde5fd4a1.png)

# Competition

- Neurons calculate respective values for given input using discriminant function
- Highest value wins

# Cooperation

- Winner defines neighbourhood of surrounding neurons to be excited
	- Use Gaussian to define neighbourhood and level of influence
 ![Exported image](../../../img/OneNote/SOFM%20image%20b7c3e2b6286c8712.png)  
![Exported image](../../../img/OneNote/SOFM%20image%2073d1a649cf221a4e.png)

- Decay the neighbourhood over time
 ![exp](../../../img/OneNote/SOFM%20image%2015ba85fc609eb1d0.png)

- Neighbourhood function
 
# Synaptic adaptation

- Excited neurons increase individual values of discriminant function
	- In relation to input pattern
	- By adjusting weights
		- To increase response of winning neuron
 ![Exported image](../../../img/OneNote/SOFM%20image%20d13b1236ff6bc54f.png)

- Forgetting term
 ![Exported image](../../../img/OneNote/SOFM%20image%203e83497d21a1d741.png)

- First term is Hebbian
- Second is forgetting
 ![Exported image](../../../img/OneNote/SOFM%20image%2068edd90aef196ee6.png)

- To satisfy first requirements
- Linear function
 ![Exported image](../../../img/OneNote/SOFM%20image%20d8ae0d1c44d5a74c.png)

- Further simplify
	- Just the neighbourhood function
 ![Exported image](../../../img/OneNote/SOFM%20image%20e98d34ee58e5612e.png)  
![Exported image](../../../img/OneNote/SOFM%20image%20188650676405d6b3.png)

- For all neurons in lattice within neighbourhood
- For repeated training the weight vectors follow the distribution of the input vectors
	- Due to the neighbourhood updating
	- Neighbouring neurons will have similar synaptic weight vectors
 ![1111 Tloexp](../../../img/OneNote/SOFM%20image%2060684c4a436d578c.png)

- Exponentially decay learning rate

![1. Initialization. Choose random values for the in...](../../../img/OneNote/SOFM%20image%201a2e5f3271456d43.png)

![Property L Approximation of the Input Space. The f...](../../../img/OneNote/SOFM%20image%2048e1489e74d290ef.png)  
![Property 2. Topological Ordering. The feature map ...](../../../img/OneNote/SOFM%20image%20f8759561e916ebf3.png)  
![Property 3. Density Matching. The feature map refl...](../../../img/OneNote/SOFM%20image%2001a95ff3818227fb.png)  
![Property 4. Feature selection. Given data from an ...](../../../img/OneNote/SOFM%20image%202dd0c4fad45b24d7.png)  

2D
 ![0.8 0.6 0.4 0.2 0.6 0.5 0.2 0.1 0.1 0.2 0.8 0.6 0....](../../../img/OneNote/SOFM%20image%2020101737fd731b1a.png)

1D
 ![0.8 .. 0.6 0.2 0.8 0.6 0.4 0.2 FIGURE 9.9 0.5 0.5 ...](../../../img/OneNote/SOFM%20image%205912954940f423b8.png)

