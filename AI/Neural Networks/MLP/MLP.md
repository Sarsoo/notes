---
tags:
  - ai
---
-   [Feedforward](../Architectures.md)
-   Single hidden layer can learn any function
	-   Universal approximation theorem
-   Each hidden layer can operate as a different feature extraction layer
-   Lots of [weights](../Weight%20Init.md) to learn
-   [Back-Propagation](Back-Propagation.md) is [supervised](../../Learning.md#Supervised)

![mlp-arch](../../../img/mlp-arch.png)

# Universal Approximation Theory
A finite [feedforward](../Architectures.md) MLP with 1 hidden layer can in theory approximate any mathematical function
-   In practice not trainable with [BP](Back-Propagation.md)

![activation-function](../../../img/activation-function.png)
![mlp-arch-diagram](../../../img/mlp-arch-diagram.png)
## Weight Matrix
-   Use matrix multiplication for layer output
-   TLU is hard limiter
![tlu](../../../img/tlu.png)
- $o_1$ to $o_4$ must all be one to overcome -3.5 bias and force output to 1
![mlp-non-linear-decision](../../../img/mlp-non-linear-decision.png)
- Can generate a non-linear [decision boundary](Decision%20Boundary.md)