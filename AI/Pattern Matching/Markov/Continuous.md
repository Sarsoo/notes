---
onenote-id: 0-841e3949b29f0610120e7dea2d6a1588!1-D084F068F621FF9!3714
---
Discrete observations previously

- Red, green, blue

Continuous

- Floating point numbers
- Coefficients
- Come from PDF
 
- Markov chain gives flexibility in time
	- Outputs gives flexibility in observations

B matrix changes  
A stays the same  
 $$b_i(o_t)=p(o_t|x_t=i)$$

# Scalar
$$b_i(o_t)=\mathcal{N}(o_t,\mu_i,\Sigma_i)$$
$$=\frac{1}{\sqrt{2\pi\Sigma_i}}exp\left(\frac{-(o-\mu_i)^2}{2\Sigma_i}\right)$$

- Evaluated at $o_t$
- Sigma is variance
 
# Multi-Variate
$$b_i(o_t)=\frac{1}{\sqrt{(2\pi)^K\left|\Sigma_i\right|}}exp\left[-\frac{1}{2}(o_t-\mu_i)\Sigma_i^{-1}(o_t-\mu_i)^T\right]$$
- K-dimensional
- Pre multiply by determinant of co-variance

Continuous PDF Parameter Estimation
 
[CLASSIFIER TRAINING](../../../../../../AI/Classification/Supervised/Supervised.md)
 $$\hat{\mu}_i=\frac{\sum^T_{t=1}\gamma_t(i)o_t}{\sum^T_{t=1}\gamma_t(i)}$$
 $$\hat{\Sigma}_i=\frac{\sum^T_{t=1}\gamma_t(i)(o_t-\mu_i)(o_t-\mu_i)^T}{\sum^T_{t=1}\gamma_t(i)}$$

Log Probabilities
 
# Scalar

![biot Not 01 li 2](../../../../img/OneNote/Continuous%20image%20743d1bf28041d54a.png)  

# Multi-Variate

![biot Not 1 2 1 2 ot 2 1 ot lliT lliT](../../../../img/OneNote/Continuous%20image%202e7489660e377c62.png)  

Viterbi
 ![1. Initially at t 1, ln 51 i ln bi 01 Oli o 2. For...](../../../../img/OneNote/Continuous%20image%20242d7b4d8898a43f.png)