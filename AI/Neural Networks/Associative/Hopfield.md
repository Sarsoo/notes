---
onenote-id: 0-2c9f850886810e1c0c6b1bae70baa776!1-D084F068F621FF9!3714
---
![Ndim network, N 3 12](../../../../img/OneNote/Hopfield%20image%20c0c96db6b8e30e6d.png)

Single Layer Feedback

- Undirected connections
- Output connected to all other neurons
- Non-linear associative memory
- Binary outputs
- Stable states are complements
- Good for constraint satisfaction problems
- Same number of units as dimensionality of training data
- Unsupervised model
- Content-addressable memory

![Si e 1,1, s is the state vector](../../../../img/OneNote/Hopfield%20image%20692710a84bb5e552.png)

![Let patterns to be memorised be given by 41 1,2,.....](../../../../img/OneNote/Hopfield%20image%2084f2c4ce8c53c077.png)

- Asynchronous update
	- Picking single random neuron and change state
- Synchronous
	- Change more than one neuron's state
 
- Learn weights to capture positive and negative relationships among attributes of training data
	- Energy function
		- Loss function in traditional feed-forward stuff
		- Minimising encourages node pairs with large positive weights to have similar states and vice versa
- Learn by minimising energy using weights when network state fixed to training data

![weights 23 or 23 1 Example N 3 2 stable states wei...](../../../../img/OneNote/Hopfield%20image%200c7804058df16f8f.png) ![Exported image](../../../../img/OneNote/Hopfield%20image%209f7147c21321b942.png)

![Exported image](../../../../img/OneNote/Hopfield%20image%20d8055180773517a2.png)

- States
 ![E Y..nsj](../../../../img/OneNote/Hopfield%20image%207ab47a1d20b698d3.png)

- First term encourages units with large biases to be on
- Second term encourages to states to be similar when weight greater than 0
	- Positive weights cause state attraction
	- Negative weights cause state repulsion
- For small training data
	- Memorises
	- States can be retrieved from corrupt or noisy query points
		- Explores local minima of E nearby
- Final state is often a member of the training data
	- Not always
		- Spurious minima
 ![Exported image](../../../../img/OneNote/Hopfield%20image%20ee2d2306fa32de82.png)

- Difference in energy between two states
 ![1 ifE jji 0 0 Otherwise](../../../../img/OneNote/Hopfield%20image%20d29e5ad7a9ab4431.png)

- Must be larger than 0 to flip state from 0 to 1
 
- Starts generalising instead of memorising when amount of data exceeds capacity of model
	- Stores representative cluster centres

Uses
 
- Recalling associative memories
	- Apply target input
	- Final state = output
- Correcting corrupted data
	- Similar to above
	- Apply corrupted input
	- Final state = output
- Attribute completion
	- Set known attributes
		- Unknown randomly
	- Update _unknown_ states until convergence

Training
 
- Hebbian
 ![Exported image](../../../../img/OneNote/Hopfield%20image%208e31261b3da8d86e.png)

- $j$ -th bit of $i$ -th training point
- For  
	training points
 ![Exported image](../../../../img/OneNote/Hopfield%20image%206461e82d6534f827.png)

- Positively correlated bits  
	and  
	are will be cause numerator positive
 ![Exported image](../../../../img/OneNote/Hopfield%20image%20a2c5212d1ca624fc.png)

- Iterative updates
 ![Exported image](../../../../img/OneNote/Hopfield%20image%20f8f780b8df62935f.png)

- Bias assumed single dummy state always on
 ![4 Xki.TkJ , b Xki](../../../../img/OneNote/Hopfield%20image%20a6357548f787a16b.png)

- State vectors from