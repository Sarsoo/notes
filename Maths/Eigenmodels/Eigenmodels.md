---
onenote-id: 0-91995b20d2a34011a72d2892c5e04045!1-D084F068F621FF9!4116
---
Make model fit data by capturing mean and spread of data

Variance
 
Single number encoding spread about mean, s.d. squared
 $𝜇 = \frac{1}{n} \sum_{i = 1}^{n} x_{i}$  
$𝜎^{2} = \frac{1}{n} \sum_{i = 1}^{n} \left(x_{i} - 𝜇\right)^{2}$

Covariance
 
DxD matrix, C, encoding spread about mean in D dimensions
 $x = \begin{bmatrix} x_{1} & \ldots & x_{n} \\ y_{1} & \ldots & y_{n} \end{bmatrix}$ $𝜇 = \frac{1}{n} \sum_{i = 1}^{n} x_{i}$ $C = \frac{1}{n} \left(x - 𝜇\right) \left(x - 𝜇\right)^{T}$  

# Decompose

_Factorise_ covariance matrix

- Eigenvalue Decomposition
	- $C = U V U^{T}$
	- U = Vectors
	- V = Values

$C = U V U^{T}$

![Machine generated alternative text c 3x3 Covarianc...](../../img/OneNote/Eigenmodels%20image%20cd413aeb001d0879.png)

Mahalanobis Distance
 $d^{2} = \left|V^{- 1} U^{T} \left(x - 𝜇\right)\right|$         $d^{2} = \left(x - 𝜇\right)^{T} C^{- 1} \left(x - 𝜇\right)$
                    
                
                   

![Machine generated alternative text So to project y...](../../img/OneNote/Eigenmodels%20image%204f00b7a5e3ca1d87.png)

