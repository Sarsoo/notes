---
onenote-id: 0-8b227f02f47306e4071b453807eb4918!1-D084F068F621FF9!3691
---
# A/D Conversion
- Sampling
	- From x(t) to x[n]=x(nT)
	- Every T seconds
	- Sample & hold
	- Sample frequency is one over T
	- Quantise along x
- Quantisation
	- Discrete number of different values
		- Quantisation levels
	- Difference to original is _quantisation_ error
	- Quantise up y
 ![Machine generated alternative text afd antialiasin...](../../img/OneNote/A-D%20image%20f26f4ffaecda76c7.png)

# Dynamic Range
- Dynamic range of clean speech is around 40 dB
- Background noise is rough when SNR \> 30 dB
- 70 dB range provides reasonable quality
	- 12-bit resolution
	- 6 dB/bit
 
- CD quality
	- 16 bit
	- 96 dB dynamic range
 
- DAW
	- \< 24-bit

# Aliasing
- Multiple frequencies can fit same set of quantised points
- Nyquist
	- Frequency
		- Half of sampling frequency
		- Above which sound will be aliased
	- Criterion
		- Sampling frequency must be twice as high as highest frequency in sound
- Anti-aliasing
	- Cut frequencies above Nyquist frequency
	- Before sampling
- Oversampling
	- Filter of required steepness is hard
	- Sample above required signal in order to reduce aliasing above fn
 ![Exported image](../../img/OneNote/A-D%20image%20a82e39a89ec922aa.png)  
![e q](../../img/OneNote/A-D%20image%204a4ec6f7208989e0.png)

- b shows overlap, copies, aliases

# D/A Conversion
- Deglitching
- Interpolating
	- Low-pass to remove sharp edges
		- High frequency noise
	- Sampling theorem says use sinc impulse filter
		- In reality must be truncated
 ![2its](../../img/OneNote/A-D%20image%20765e1b6003496d44.png)
 
# Compressed Sensing
- Sparse representation

# Discrete Time
- DT signals usually gathered from a CT signal
	- ADC
- $x_{n} = x \left(n T\right)$
	- $\forall n \in \mathbb{Z}$
	- T = sampling period
- Run through Nyquist filter first
	- Low pass filter for frequencies above _folding frequency_
		- $1/\left(2 T\right)$
	- No information in filtered signal lost
	- Prevents aliasing

$x_{n} = x \left(n T\right)$ $\forall n \in \mathbb{Z}$ $1/\left(2 T\right)$