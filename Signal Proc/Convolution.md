---
tags:
  - signals
  - maths
---
Integral operator
-   Satisfies mathematical properties of integral operator
-   Product of two after one has been reversed and shifted

$$x(t)=x_1(t)\circledast x_2(t)=\int_{-\infty}^\infty x_1(t-\tau)\cdot x_2(\tau)d\tau$$

# Properties
1. $x_1(t)\circledast x_2(t)=x_2(t)\circledast x_1(t)$
	- Commutativity
2. $(x_1(t)\circledast x_2(t))\circledast x_3(t)=x_1(t)\circledast (x_2(t)\circledast x_3(t))$
	- Associativity
3.  $x_1(t)\circledast [x_2(t)+x_3(t)]=x_1(t)\circledast x_2(t)+ x_1(t)\circledast x_3(t)$
	- Distributivity
4. $Ax_1(t)\circledast Bx_2(t)=AB[x_1(t)\circledast x_2(t)]$
	- Associativity with Scalar
5. Symmetrical graph about origin
6. $y(t)=x_1(t-a)\circledast x_2(t-b)$
	- $x(t)=x_1(t)\circledast x_2(t)$
	- $y(t)=x(t-a-b)$
7. $x(t)=x_1(t)\circledast x_2(t)$
	- $x_1$ between $a_1$ and $b_1$
	- $x_2$ between $a_2$ and $b_2$
	- Starting point of $x(t)=a_1+a_2$
	- Ending point of $x(t)=b_1+b_2$
8. $\overline{x \circledast y}=\bar x \circledast \bar y$
9. $(x \circledast y)'=x'\circledast y=x\circledast y'$

# Applications
1. Communications systems
	- Shift signal in frequency domain (Frequency modulation)
2. System analysis
	- Find system output given input and [transfer function](Transfer%20Function.md)

# Polynomial Multiplication
-   Convolving coefficients of two poly gives coefficients of product

# Discrete
$$G[i,j]=H[u,v]\circledast F[i,j]$$
$$G[i,j]=\sum^k_{u=-k}\sum^k_{v=-k} H[u,v]F[i-u,j-v]$$