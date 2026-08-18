---
tags:
  - maths/signals
  - maths
---
# Integral operator
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

# Polynomial Multiplication
- Convolving coefficients of two poly gives coefficients of product

# Correlation
$$c\left[m\right]=\frac{1}{N}\sum\limits_{n=0}^{N-1}s\left[n\right]t\left[n+m\right]$$
- Statistical measure of similarity
- One shifted across the other
	- Basically convolution
		- No time reversal

# Autocorrelation
$$R\left[m\right]=\frac{1}{N}\sum\limits_{n=0}^{N-1}s\left[n\right]s\left[n+m\right]$$
- X-Correlation with itself
- Largest value at zero-lag
	- Average power of signal
$$R\left[0\right]=\frac{1}{N}\sum\limits_{n=0}^{N-1}s\left[n\right]^2$$
- Generally decreases over time ($m$ increases)
- Peaks indicate periodicity
	- Minimise amplitude difference
$$E[\tau]=\frac{1}{N}\sum_{n=0}^{N-1}\left(s[n]-\beta s[n+\tau]\right)^2$$
	- Maximise normalised auto-correlation
$$R[\tau]=\frac{1}{N}\frac
{\sum_{n=0}^{N-1}s[n]s[n+\tau]}
{\sqrt{\sum_{n=0}^{N-1}s\left[n+\tau\right]^2}}$$
	- Only need to check certain range of lags for speech
		- m = sample freq / fundamental freq
		- Sample = 60 Hz for male, 600 Hz for children
- PSD of speech is DFT of autocorrelation
$$DFT\{R[m]\}=P[k]=DFT\{s[n]\}DFT^*\{s[n]\}/N$$