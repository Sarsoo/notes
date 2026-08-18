---
onenote-id: 0-c7bb5d47016b0cc5010a57abf5828db6!1-D084F068F621FF9!3707
---
ARMA  
Autoregressive Moving Average
 $s \left[n\right] = - \sum_{k = 1}^{p} a_{k} s \left[n - k\right] + \sum_{j = 0}^{q} b_{j} u \left[n - j\right]$

- Output is weighted average of past outputs, inputs and the current input
- Pole-zero filtering
 $s \left[n\right] = - \sum_{k = 1}^{p} a_{k} s \left[n - k\right] + b_{0} u \left[n\right]$

- AR
	- Autoregressive
- All-pole filter
 $s \left[n\right] = \sum_{j = 0}^{q} b_{j} u \left[n - j\right]$

- MA
	- Moving average
- All-zero filter

$H \left[z\right] = \frac{G}{1 + \sum_{k = 1}^{p} a_{k} z^{- k}}$  

- Future values estimated as weighted summation of previous samples
	- Discrete-time
- Auto-regressive
	- All-pole
		- Nasals & fricatives can cause anti-resonances
			- Would use pole-zero
			- High order is good approximation
- Exploit redundancy between consecutive samples
	- Encode & transmit critical information
 
# Predictor Output

$\hat{s} \left[n\right] = - \sum_{k = 1}^{p} a_{k} s \left[n - k\right]$  

# Error

$e \left[n\right] = s \left[n\right] - \hat{s} \left[n\right] = s \left[n\right] + \sum_{k = 1}^{p} a_{k} s \left[n - k\right]$

# Coefficient Calculation

$E \left{e^{2} \left[n\right]\right} = E \left{\left(s \left[n\right] + \sum_{k = 1}^{p} a_{k} s \left[n - k\right]\right)^{2}\right}$

- Minimise above

[DSP Related - Matlab, Simplest Lowpass](https://www.dsprelated.com/freebooks/filters/Matlab_Analysis_Simplest_Lowpass.html)

[Linear Predictive Coding is All-Pole Resonance Modeling - Stanford](https://ccrma.stanford.edu/~hskim08/lpc/)
 
_"All-Pole Resonance Modelling"_
 
- Each pole corresponds to a delay
	- System has memory
	- Current sample result of current input with past samples
- All-pole approach known as auto-regression
	- Finding future value of itself from past

Z Transform?

Estimate
 
- Autocorrelation
	- Yule-Walker
	- ![Rn pl RnP2 Rn 0 Rnl Rnl Rn0 Rnp2 Rn2 RnP1 Rn 1 Rn ...](../../../../img/OneNote/Linear%20Prediction%20image%2028a93be1f336b355.png)
      
	- ![NIJ Rnj](../../../../img/OneNote/Linear%20Prediction%20image%20606e93f017399aff.png)
	- Toeplitz matrix
		- Solve using Durbin's algorithm
- Covariance
	- ![np l np 2 2 l 2 2 1 l 1 2 p,0 2 0](../../../../img/OneNote/Linear%20Prediction%20image%20ee486af11a3cdb7a.png)
      
	- ![m](../../../../img/OneNote/Linear%20Prediction%20image%20debd36ab5f89e336.png)
	- Not Toeplitz
		- Matrix inversion
   

Inverse Filtering
 
- Obtain excitation signal
 $S \left(z\right) = H \left(z\right) U \left(z\right)$ $U \left(z\right) = H^{- 1} \left(z\right) S \left(z\right) = A \left(z\right) S \left(z\right)$  

- A is the inverse filter
- Residual
	- Voiced/unvoiced
	- Periodicity
	- Auto-correlate

![8L0 S!113 8 nos SWOZ](../../../../img/OneNote/Linear%20Prediction%20image%20ba313385562abc8f.png)

Synthesis
 ![Machine generated alternative text Encoder Filter ...](../../../../img/OneNote/Linear%20Prediction%20image%20be8083244671fb88.png)  

- LPC coefficients for filter response
- Residual for fundamental frequency
 
- Generate impulse train for excitation
- Use LPC as all-pole

Poor fit to spectral valleys
