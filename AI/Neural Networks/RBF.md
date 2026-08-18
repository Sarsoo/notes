---
onenote-id: 0-004fc458b1e10c3c39d41fece166317a!1-D084F068F621FF9!3714
---
- Alternative to backpropagation
- Classification/regression
- Classifies non-separable patterns using two stages
	- Non-linear followed by linear
- Universal approximator
- Good interpolator
	- Less so for extrapolating
- Supervised

![First stage is to transform patterns into new spac...](../../../img/OneNote/RBF%20image%205af6fde61f51aaad.png)

- Neurons are Gaussian functions
	- Measure distance from input to centre
- Then linearly separate
- Very different to MLP
- Centre functions on training data

XOR Problem
 
- Simplest 2D function which is non-separable
- Doesn't increase dimensionality of the input space
	- Non-linearity of RBF is enough to transform XOR into a linearly separable problem
 ![QIE 1 1 patterns 0,1 1,0 till t2112, pattern 0,0 d...](../../../img/OneNote/RBF%20image%2042342e0533a2a946.png)  
![Input nodes Gaussian functions fixed input 1 b bia...](../../../img/OneNote/RBF%20image%20433c990c7c8a5eb8.png)  
![till t 12, i 1,2](../../../img/OneNote/RBF%20image%205d6ea0bccd4fe190.png)  
![2 OJT](../../../img/OneNote/RBF%20image%202672d9e17200d784.png)  
![Flx 2x 1, IIT](../../../img/OneNote/RBF%20image%20a99f380b5579e245.png)  
![yx wGlx ti b](../../../img/OneNote/RBF%20image%20373f484e69474f30.png)  
![1 , 2 , 3 , 4](../../../img/OneNote/RBF%20image%205e3fdb8b7c1dfc39.png)  
![gji Glxj fili,](../../../img/OneNote/RBF%20image%20e7df86d1d0102c9e.png)  
![Exported image](../../../img/OneNote/RBF%20image%2060cca703613a8d72.png)  
![1 0.3678 0.1353 0.3678 0.1353 0.3678 1 0.3678 1 1 ...](../../../img/OneNote/RBF%20image%2084a32c7bbce5fcfe.png)  

- Output layer
	- Use weight-sharing
		- Problem is symmetric
		- Prior information being built into network
	- Uses bias
		- Data independent
- Overdetermined problem
	- More data points than free parameters
		- G not square
		- No unique inverse exists for G
		- Use minimum norm solution
 ![GTG1GTd](../../../img/OneNote/RBF%20image%20afa11bc2e71de419.png)  
![G L8292 0 , 6727 0.9202 L2509 1.2509 t4202 6727 L8...](../../../img/OneNote/RBF%20image%20174e9a363c9fb555.png)  
![25018 w 25018 2.8404](../../../img/OneNote/RBF%20image%20bf7c6b13f468602e.png)  

_Finding a surface in multidimensional space that provides a best fit to the training data_

![1.0 0.6 0.2 Decision boundary 02 0.4 0.6 91 b 1.0 ...](../../../img/OneNote/RBF%20image%203acc64d896079afa.png)

Interpolation Problem
 
- For hidden functions centred on every training pattern
	- Gives perfect interpolation
	- However training data is likely noisy
		- Not necessarily the goal
	- Thus reduce power of network
		- Can just lower number of hidden functions
		- Or change standard deviations of Gaussian functions
			- Broaden
 ![ors uO!J!puOO. u0?1Dl0daanz? 2111 sPDs!S7 n1 uopun...](../../../img/OneNote/RBF%20image%200245e32fc1de4b99.png)  
![Fx Xill](../../../img/OneNote/RBF%20image%206ebc9d6c82a72154.png)  
![21 12 22 2 2 Q.C2 N 12](../../../img/OneNote/RBF%20image%20f98b6c596d661408.png)  
![vllxj x,ll, d dl,d2, ...,dN WI, u,2, ..., WNT](../../../img/OneNote/RBF%20image%204b649c7c3439f0a8.png)  
![1,2, ...,N](../../../img/OneNote/RBF%20image%2001fe70baa7e24ecb.png)  
![Exported image](../../../img/OneNote/RBF%20image%2093791e49e9d3c35f.png)  
![Exported image](../../../img/OneNote/RBF%20image%20f27747b81a01aff0.png)  

Micchelli's Theorem
 ![Let be a set of distinct points in Rmo. Then the N...](../../../img/OneNote/RBF%20image%2065b380dd8303f3f2.png)  

- Holds for below
 ![1. Multiquadrics r r2 c2l2 for some c O and r R 2....](../../../img/OneNote/RBF%20image%20b9dbec77b5e995e6.png)

- And SVMs

Regularisation
 ![Input signal Desired response](../../../img/OneNote/RBF%20image%20e7d3498ad3f1078b.png)  
![1. Standard Error Term. This first term, denoted b...](../../../img/OneNote/RBF%20image%2043beb78690496f02.png)  

Cover's Theorem on the Separability of Patterns
 
_A complex pattern-classification problem cast in a high-dimensional space nonlinearly is more likely to be linearly separable than in a low-dimensional space_

Hidden Functions instead of Hidden Units

Learning
 
- How to centre Gaussians
	- Treat as unsupervised learning
	- Similar to SOFM

Compare to MLP
 
|   |   |
|---|---|
|# MLP|# RBF|
|Possibly multiple hidden layers|Single hidden layer|
|Common neuron models throughout|Hidden neurons are different to output neurons|
|Typically nonlinear throughout|Nonlinear hidden layer, linear output layer|
|Inner product of input vector and synaptic weight vector|Euclidean distance between training pattern and unit centre|
|Global approximations to nonlinear input-output mapping<br><br>  <br><br>Good at extrapolation|Local approximations to non-linear input-output mappings￼￼Fast learning but poor extrapolation|