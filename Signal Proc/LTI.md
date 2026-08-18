---
onenote-id: 0-896c7fb402134741925e72a8e9064b49!1-D084F068F621FF9!3691
---
# IRF - Impulse Response Function 
- Output following impulse
- Generally functions as response of dynamic system to external change
- System reaction as function of time (or independent variable)
- Impulse function contains all frequencies
	- Response defines LTI response for all frequencies
# IIR - Infinite Impulse Response
- $h \left(t\right)$ not zero past certain point
	- Continues indefinitely
# FIR - Finite Impulse Response
- $h \left(t\right)$ has finite duration, becomes zero

# [Linear Time Invariant (LTI)](https://en.wikipedia.org/wiki/Linear_time-invariant_system)
`Linear & Time Invariant`
- Linear
	- Input to output described by **Linear Differential Equations**
	- [Superposition Principle](https://en.wikipedia.org/wiki/Superposition_principle)
- Time Invariant
	- Output does not depend on specific time input is applied
	- $x \left(t\right) \rightarrow y \left(t\right)$
		- $x \left(t - T\right) \rightarrow y \left(t - T\right)$  

- Time domain described by **impulse response**
	- System output, y(t) is convolution of impulse response with input
	- _Continuous time system_
- Frequency domain described by **transfer function**
 
- Transfer function is Laplace transform of Impulse response
	- Z-transform if discrete
 [![Time domain xt zaplace ht zaplace](../../img/OneNote/LTI%20image%20065844ba0921e39e.png)](https://en.wikipedia.org/wiki/File:LTI.png)  
- LTI systems cannot produce frequency components that are not in the input
 
## Properties
- Causality
	- Output depends on current and past values
- Stability
	- **Bounded input, Bounded output stable (BIBO)**
		- Finite input -\> finite output

