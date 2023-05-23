-   Feed-forward
-   Single hidden layer can learn any function
	-   Universal approximation theorem
-   Each hidden layer can operate as a different feature extraction layer
-   Lots of weights to learn
-   [[Back-Propagation]] is supervised

![[mlp-arch.png]]

# Universal Approximation Theory
A finite feed-forward MLP with 1 hidden layer can in theory approximate any mathematical function
-   In practice not trainable with [[Back-Propagation|BP]]

![[activation-function.png]]
![[mlp-arch-diagram.png]]
## Weight Matrix
-   Use matrix multiplication for layer output
-   TLU is hard limiter
![[tlu.png]]
- $o_1$ to $o_4$ must all be one to overcome -3.5 bias and force output to 1
![[mlp-non-linear-decision.png]]
- Can generate a non-linear [[Decision Boundary|decision boundary]]