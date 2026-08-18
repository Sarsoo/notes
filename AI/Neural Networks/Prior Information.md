- No set rules
 
1. Restrict network architecture through local connections
	- _Receptive fields_
2. Constraining choice of weights through _weight-sharing_
 
- Reduces free parameters
 ![Input layer Layer of hidden neurons Layer Ot ourpu...](../../../img/OneNote/Neural%20Networks%20image%20f6a41cdfc948b782.png)

- Only top six source neurons connected to H1
	- Receptive field for H1
- Weight sharing uses same set of weights for each hidden neuron
 $$v_{j} = \sum_{i = 1}^{6} w_{i} x_{i + j - 1} ,   j = 1 , 2 , 3 , 4$$ 

- $\{w_{i}\}_{i = 1}^{6}$ shared set of weights
- Convolutional sum
 
Feedforward network using local connections and weight-sharing  
_Convolutional Network_