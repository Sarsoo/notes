---
title: 'Markov Chains'
tags:
  - ai
  - maths
---
[Hidden Markov Models - JWMI Github](https://jwmi.github.io/ASM/5-HMMs.pdf)
[Rabiner - A Tutorial on Hidden Markov Models and Selected Applications in Speech Recognition](https://www.cs.cmu.edu/~cga/behavior/rabiner1.pdf)

- Stochastic sequences of discrete states
	- Transitions have probabilities
- Desired output not always produced the same
	- Same pronunciation

![](../../../img/markov-state.png)

$$P(X|M)=\left(\prod_{t=1}^Ta_{x_{t-1}x_t}\right)\eta_{x_T}$$
$$a_{x_0x_1}=\pi_{x_1}$$

# 1st Order
- Depends only on previous state
	- Markov assumption

$$P(x_t=j|x_{t-1}=i,x_{t-2}=h,...)\approx P(x_t=j|x_{t-1}=i)$$

- Described by state-transition probabilities

$$a_{ij}=P(x_t=j|x_{t-1}=i), 1\leq i,j\leq N$$

- $\alpha$
	- State transition
- For $N$ states
	- $N$  by $N$ matrix of state transition probabilities

# Weather

![](../../../img/markov-weather.png)
$$A=\left\{a_{ij}\right\}=\begin{bmatrix} 0.4 & 0.3 & 0.3\\ 0.2 & 0.6 & 0.2 \\ 0.1 & 0.1 & 0.8 \end{bmatrix}$$
rain, cloud, sun across columns and down rows
$$A=\{\pi_j,a_{ij},\eta_i\}=\{P(x_t=j|x_{t-1}=i)\}$$

# Start/End
- Null states
	- Entry/exit states
	- Don't generate observations

![](../../../img/markov-start-end.png)
$$\pi_j=P(x_1=j) \space 1 \leq j \leq N$$
- Sub $j$ because probability of kicking off into that state
$$\eta_i=P(x_T=i) \space 1 \leq i \leq N$$
- Sub $i$ because probability of finishing from that state

![](../../../img/markov-start-end-probs.png)
![](../../../img/markov-start-end-matrix.png)

# State Duration
- Probability of staying in state decays exponentially
$$p(X|x_1=i,M)=(a_{ii})^{\tau-1}(1-a_{ii})$$
![](../../../img/markov-state-duration.png)
- Given, $a_{33}=0.8$
- $\times0.8$ repeatedly
	- Stay in state

# Hidden
![Exported image](../../../img/OneNote/Markov%20image%20b07490ac5f77f316.png)

# Discrete
$$b_i(o_t)=P(o_t=k|x_t=1)$$
- $b$ = output
# Continuous
$$b_i(o_t)=p(o_t|x_t=1)$$
Subscript indicates state outputting from
![al I a44 an an a34 114 b Ioi b03 b9 b 102 bQD gene...](../../../img/OneNote/Markov%20image%20a2b603a1af888eb2.png)
$$P(O,X|\lambda)=P(X|\lambda)P(O|X,\lambda)$$
- Probability of state sequence and observations
	- States given model times observations given states
- Either two sequences
	- States given model
	- Observations given states
- Or as a whole
	- State transition
	- Observation given state
	- Iterate
![0.8 0.6 1.0 0.2 0.4 2 01 02 03](../../../img/OneNote/Markov%20image%20992b1ebfc126c0f4.png)
![1 0.8 0.2 0.6 R 0.5 0.4 G 0.2 0.9 0.3 0.1](../../../img/OneNote/Markov%20image%205b7fd49b5b8e1903.png)
$X = \left(1 , 2 , 2\right)$ 
$$P \left(O , X \left|\right. \lambda\right) = \left(\prod_{t = 1}^{T} a_{x_{t - 1} x_{t}} b_{x_{t}} \left(o_{t}\right)\right) 𝜂_{x_{T}}$$ 
$$=\pi_1b_1(o_1)a_{12}b_2(o_2)a_{22}b_2(o_3)\eta_2$$
$= 1 \times 0 . 5 \times 0 . 2 \times 0 . 9 \times 0 . 6 \times 0 . 9 \times 0 . 4$
