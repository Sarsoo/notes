---
onenote-id: 0-00ba55a87b8e02911949d9fee364530c!1-D084F068F621FF9!3714
---
![stimulus ak WII aki wp ak2 a kp response bk2 bkp](../../../img/OneNote/Associative%20image%20c471008d6ad2ce30.png)

![bkl bk2 bkp vpl k vvp2 k akl ak2 akp wpp k](../../../img/OneNote/Associative%20image%20e7b09a3f9d6efb70.png)

- Estimate weight matrix
	- $\sum_{k} \underset{̲}{b}_{k} \underset{̲}{a}_{k}^{T}$
	- For k from 1 to q
	- Hebbian learning

$\sum_{k} \underset{̲}{b}_{k} \underset{̲}{a}_{k}^{T}$

![For recall of a stimulus pattern aj assuming that ...](../../../img/OneNote/Associative%20image%20f697ad9325dfc825.png)

- Distributed memory
- No activation function
- Auto and hetero-associative
	- Different stimulus-response pair
	- Auto
		- A = b
- Content addressable
	- Input that stimulates output
	- Resistant to noise and damage
- Interaction between stored patterns
	- May lead to error in recall
- Can recall  
	patterns
	- $p$ is the rank of the matrix
- For auto-associative
	- $W a_{k} = a_{k}$
		- Stimulus patterns are eigenvectors of W with all unity eigenvalues

$W a_{k} = a_{k}$

![Example bl 15 1 OIT, b2 memory weight matrix 5 22 ...](../../../img/OneNote/Associative%20image%207ef59c7974a2bb49.png)

Single Layer Feedforward

![Input layer Synaptic Output layer Of neurons junct...](../../../img/OneNote/Associative%20image%2077b8d5957ed3bf44.png)

- Assumed to be linear
- Neuron acts as a linear combiner

Correlation Matrix Memory
 $\hat{\mathbf{M}} = \sum_{k = 1}^{q} y_{k} x_{k}^{T}$  

- Estimate of the memory matrix,  
    
- Outer product of key pattern,  
	, and memorise pattern,  
	- Estimate of the weight matrix, $w \left(\right. k \left.\right)$ , that maps the output pattern onto input
- _m_-by-_m_ matrix
	- Dimensionality matches M
- $x_{k j}$ is the output of node $j$ the input layer
- $y_{k i}$ is output of node $i$ in the output layer
	- For  
		th association
		- $j$ acts as presynaptic node
		- $i$ acts as postsynaptic node
		- Local learning process similar to a generalised Hebb's postulate
 $\hat{\mathbf{M}} = \left[y_{1} , y_{2} , \ldots , y_{q}\right] \begin{bmatrix} x_{1}^{T} \\ x_{2}^{T} \\ \vdots \\ x_{q}^{T} \end{bmatrix}$ $= \mathbf{Y} \mathbf{X}^{T}$  

Where
 $\mathbf{X} = \left[x_{1} , x_{2} , \ldots , x_{q}\right]$  

And
 $\mathbf{Y} = \left[y_{1} ,  y_{2} ,  \ldots ,  y_{q}\right]$  
$\hat{\mathbf{M}}_{k} = \hat{\mathbf{M}}_{k - 1} + y_{k} x_{k}^{T} ,   k = 1 ,  2 ,  \ldots , q$

$\underset{̲}{b}_{k} = \mathbf{W} \left(k\right) \underset{̲}{a}_{k}$

$𝒚_{k} = \mathbf{W} \left(k\right) \cdot 𝐱_{k} ,   k = 1 ,  2 ,  \ldots ,  q$  
$y_{k i} = \sum_{j = 1}^{m} w_{i j} \left(k\right) \cdot x_{k j} ,   i = 1 ,  2 ,  \ldots ,  m$  
$y_{k i} = \left[w_{i 1} \left(k\right) ,  w_{i 2} \left(k\right) ,  \ldots ,  w_{i m} \left(k\right)\right] \begin{bmatrix} x_{k 1} \\ x_{k 2} \\ \vdots \\ x_{k m} \end{bmatrix} ,   i = 1 ,  2 ,  \ldots ,  m$  
$\begin{bmatrix} y_{k 1} \\ y_{k 2} \\ \vdots \\ y_{k m} \end{bmatrix} = \begin{bmatrix} w_{11} \left(k\right) & w_{12} \left(k\right) & \ldots & w_{1 m} \left(k\right) \\ w_{21} \left(k\right) & w_{22} \left(k\right) & \ldots & w_{2 m} \left(k\right) \\ \vdots & \vdots & \vdots & \vdots \\ w_{m 1} \left(k\right) & w_{m 2} \left(k\right) & \ldots & w_{m m} \left(k\right) \end{bmatrix} \begin{bmatrix} x_{k 1} \\ x_{k 2} \\ \vdots \\ x_{k m} \end{bmatrix}$  
$\mathbf{W} \left(k\right) = \begin{bmatrix} w_{11} \left(k\right) & w_{12} \left(k\right) & \ldots & w_{1 m} \left(k\right) \\ w_{21} \left(k\right) & w_{22} \left(k\right) & \ldots & w_{2 m} \left(k\right) \\ \vdots & \vdots & \vdots & \vdots \\ w_{m 1} \left(k\right) & w_{m 2} \left(k\right) & \ldots & w_{m m} \left(k\right) \end{bmatrix}$  
$\mathbf{M} = \sum_{k = 1}^{q} \mathbf{W} \left(k\right)$  
$\mathbf{M}_{k} = \mathbf{M}_{k - 1} + \mathbf{W} \left(k\right) ,   k = 1 ,  2 ,  \ldots ,  q$  

- Above but restructured as recursion
	- As subsequent pattern contributions made
		- $W \left(\right. k \left.\right)$
		- No ability to distinguish individual contributions
	- As more patterns associated
		- Influence of any one pattern reduced

$W \left(\right. k \left.\right)$