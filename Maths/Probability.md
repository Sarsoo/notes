---
onenote-id: 0-ca53223b7e3449938ed21736f76ca07f!1-D084F068F621FF9!4116
---
Discrete
 
- Probability $P \left(X\right)$
- Histogram

Continuous
 
- Probability density $p \left(x\right)$
- Gaussian

Normalisation
 
- Discrete
	- Probability of all possible outcomes = 1
	- $\sum_{a l l  X} P \left(X\right) = 1$

$\sum_{a l l  X} P \left(X\right) = 1$  

- Continuous
	- Integral over probability density function = 1
	- $\int_{- \infty}^{\infty} p \left(x\right) d x = 1$

$\int_{- \infty}^{\infty} p \left(x\right) d x = 1$

![0.06 0.05 0.04 0.03 0.02 0.01 0.00](../img/OneNote/Probability%20image%20944596ae12c2b755.png)

Joint Probability
 
- Independent events
	- $P \left(A , B\right) = P \left(A\right) \cdot P \left(B\right) = 0 . 5 \cdot 0 . 4 = 0 . 2$
	- $A \in \left{A , \overset{-}{A}\right}$
	- $B \in \left{B , \overset{-}{B}\right}$

$P \left(A , B\right) = P \left(A\right) \cdot P \left(B\right) = 0 . 5 \cdot 0 . 4 = 0 . 2$ $A \in \left{A , \overset{-}{A}\right}$ $B \in \left{B , \overset{-}{B}\right}$  

|   |   |   |   |
|---|---|---|---|
|$P \left(A , B\right)$|$A$|$\overset{-}{A}$|$P \left(B\right)$|
|$B$|0.2|0.2|0.4|
|$\overset{-}{B}$|0.3|0.3|0.6|
|$P \left(A\right)$|0.5|0.5|1.0|
 
- Dependent events
	- $P \left(A , B\right) = P \left(A\right) \cdot P \left(B \left|\right. A\right) = 0 . 5 \cdot 0 . 2 = 0 . 1$
		- | = given, B given A
	- $P \left(A , B\right) = P \left(B\right) \cdot P \left(A \left|\right. B\right) = 0 . 4 \cdot 0 . 25 = 0 . 1$
	- Total still 1
		- Different combinations still sum to 1
		- Not simply products

$P \left(A , B\right) = P \left(A\right) \cdot P \left(B \left|\right. A\right) = 0 . 5 \cdot 0 . 2 = 0 . 1$ $P \left(A , B\right) = P \left(B\right) \cdot P \left(A \left|\right. B\right) = 0 . 4 \cdot 0 . 25 = 0 . 1$  

|   |   |   |   |
|---|---|---|---|
|$P \left(A , B\right)$|$A$|$\overset{-}{A}$|$P \left(B\right)$|
|$B$|0.1|0.3|0.4|
|$\overset{-}{B}$|0.4|0.2|0.6|
|$P \left(A\right)$|0.5|0.5|1.0|
 
# Bayes' Theorem

$P \left(H \left|\right. E\right) = \frac{P \left(E \left|\right. H\right) P \left(H\right)}{P \left(E\right)}$

- $P \left(H \left|\right. E\right) = \frac{P \left(E \left|\right. H\right) P \left(H\right)}{P \left(E\right)}$
 $P \left(w \left|\right. O\right) = \frac{P \left(O \left|\right. w\right) P \left(w\right)}{P \left(O\right)}$

- $P \left(w \left|\right. O\right) = \frac{P \left(O \left|\right. w\right) P \left(w\right)}{P \left(O\right)}$
 $P o s t e r i o r =  \frac{L i k e l i h o o d  \times P r i o r}{E v i d e n c e}$

- $P o s t e r i o r =  \frac{L i k e l i h o o d  \times P r i o r}{E v i d e n c e}$
	- Posterior
		- Basis for Bayesian inference
	- Likelihood
		- How likely are data for given class
	- Prior
		- Other knowledge
			- Language model
	- Evidence
		- _Marginal likelihood_
		- Normalises
		- Often discarded
			- Same for all

Marginalisation
 
_Marginalisation is a method that requires summing over the possible values of one variable to determine the marginal contribution of another._
 \> From \<[https://towardsdatascience.com/probability-concepts-explained-marginalisation-2296846344fc](https://towardsdatascience.com/probability-concepts-explained-marginalisation-2296846344fc)\>   
- Discrete
	- The probability of B, which depends on A
		- Sum over A of all joint probabilities
	- $P \left(B\right) = \sum_{a l l  A} P \left(A , B\right) = \sum_{a l l  A} P \left(B \left|\right. A\right) P \left(A\right)$

$P \left(B\right) = \sum_{a l l  A} P \left(A , B\right) = \sum_{a l l  A} P \left(B \left|\right. A\right) P \left(A\right)$  

- Continuous
	- $x$ is eliminated from its joint probability with $y$ by integrating
	- $p \left(y\right) = \int_{- \infty}^{\infty} p \left(x , y\right) d x = \int_{- \infty}^{\infty} p \left(y \left|\right. x\right) p \left(x\right) d x$

$p \left(y\right) = \int_{- \infty}^{\infty} p \left(x , y\right) d x = \int_{- \infty}^{\infty} p \left(y \left|\right. x\right) p \left(x\right) d x$  
![Exported image](../img/OneNote/Probability%20image%2099f801e203a0be5a.png)

Maximum Likelihood
 
- Fit gaussian to data
 $O^{t r a i n} = \left{o_{1} , o_{2} , \ldots , o_{T}\right}$

- Independent univariate Gaussian random variables
 $o_{t} \sim N \left(m , v\right)$  

# Likelihood Function

$p \left(O \left|\right. N\right) = \prod_{t = 1}^{T} \frac{1}{\sqrt{2 \pi v}} e^{- \frac{\left(o_{t} - m\right)^{2}}{2 v}}$

- Likelihood function is product of each $p \left(o_{t} \left|\right. N\right)$
- Find log likelihood function
	- Monotonic function
		- As x increases, F(x) increases
		- Reach a maximum at the same point
			- Value of m

## Log Likelihood

$L \left(m , v\right) = l n ⁡ \left[\frac{1}{\left(2 \pi v\right)^{\frac{T}{2}}} \cdot \prod_{t = 1}^{T} e^{- \frac{\left(o_{t} - m\right)^{2}}{2 v}}\right]$   $= - \frac{T}{2} l n ⁡ \left(2 \pi v\right) + \sum_{t = 1}^{T} \left(- \frac{\left(o_{t} - m\right)^{2}}{2 v}\right)$  

## Estimate Mean
 
- Differentiate log likelihood w.r.t. the mean  $\frac{𝜕 L}{𝜕 m} = \frac{𝜕}{𝜕 m} \left[- \frac{T}{2} l n ⁡ \left(2 \pi v\right) + \sum_{t = 1}^{T} \left(- \frac{\left(o_{t} - m\right)^{2}}{2 v}\right)\right]$  

￼ $= \frac{- 1}{2 v} \frac{𝜕}{𝜕 m} \sum_{t = 1}^{T} \left(o_{t} - m\right)^{2}$
   
$= \frac{1}{v} \sum_{t = 1}^{T} \left(o_{t} - m\right)$   $\frac{𝜕 L}{𝜕 m} = 0 = \hat{m}_{m l}$  
$\hat{m}_{m l} = \frac{1}{T} \sum_{t = 1}^{T} o_{t}$

- Sample mean is estimate
 
## Estimate Variance
 $\frac{𝜕 L}{𝜕 v} = \frac{𝜕}{𝜕 v} \left[- \frac{T}{2} l n ⁡ \left(2 \pi v\right) + \sum_{t = 1}^{T} \left(- \frac{\left(o_{t} - m\right)^{2}}{2 v}\right)\right]$  
$\frac{𝜕 L}{𝜕 v} = 0 = \hat{v}_{m l} = \frac{1}{T} \sum_{t = 1}^{T} \left(o_{t} - m\right)^{2}$

- Mean squared deviation
       
Log Rules

Doesn’t￼Vary

Normalisation
 ![First write Also PHIE Adding 1 and 2 gives PHIE Bu...](../img/OneNote/Probability%20image%200e4da81dfc5fcf3f.png)  

- Derive prior from data
 ![pHIE u PEIH PH .5 where u is a normalisation const...](../img/OneNote/Probability%20image%20e0b7fe52605527fa.png)  

# Conditional Independence

![where u is a normalisation constant needed to ensu...](../img/OneNote/Probability%20image%2054bdd189ff64a5e2.png)  
 
![Probability or risk Odds p pq q q](../img/OneNote/Probability%20image%20552539da77e4dc21.png)

