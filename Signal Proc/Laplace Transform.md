---
onenote-id: 0-704529daa33544cb8a3aafdfbd3e76cf!1-D084F068F621FF9!3691
---
Transfers real domain (t-domain) to complex (s-domain)

$x \left(t\right) \leftrightarrow X \left(s\right)$  

- Unilateral
	- $\mathcal{L} \left{x\right} \left(s\right) = X \left(s\right) = \int_{0}^{\infty} x \left(t\right) e^{- s t} d t$
- Bilateral
	- $\mathcal{B} \left{x\right} \left(s\right) = X \left(s\right) = \int_{- \infty}^{\infty} x \left(t\right) e^{- s t} d t$

$\mathcal{L} \left{x\right} \left(s\right) = X \left(s\right) = \int_{0}^{\infty} x \left(t\right) e^{- s t} d t$ $\mathcal{B} \left{x\right} \left(s\right) = X \left(s\right) = \int_{- \infty}^{\infty} x \left(t\right) e^{- s t} d t$  

- Inverse
	- $\mathcal{L}^{- 1} \left{X\right} \left(t\right) = x \left(t\right) = \frac{1}{2 \pi j} \int_{𝜎 - j \infty}^{𝜎 + j \infty} X \left(s\right) e^{s t} d s$

$\mathcal{L}^{- 1} \left{X\right} \left(t\right) = x \left(t\right) = \frac{1}{2 \pi j} \int_{𝜎 - j \infty}^{𝜎 + j \infty} X \left(s\right) e^{s t} d s$

_Complex Frequency, S_  
￼  
is a 2D variable,  
is 1D

- s-domain is also s-plane
 $s = 𝜎 + j 𝜔$

- _Many situations sufficient with_  
	_so_  
	- _Reduces Laplace transform with complex args to Fourier with real argument_  
        
	- _Common where interested only in steady state response of LTI_

|   |   |   |
|---|---|---|
||_t_|_s_|
|Linearity|$a f \left(t\right) + b g \left(t\right)$|$a F \left(s\right) + b G \left(s\right)$|
|t Scale|$f \left(a t\right)$|$\frac{1}{\left\|a\right\|} F \left(s/a\right)$|
|t Shift|$f \left(t - a\right) u \left(t - a\right)$|$e^{- a s} F \left(s\right)$|
|f Shift|$e^{a t} f \left(t\right)$|$F \left(s - a\right)$|
|f Derivative|$t^{n} f \left(t\right)$|$\left(\left(\right. - 1 \left.\right)\right)^{n} F^{\left(\right. n \left.\right)} \left(s\right)$|
|f Integration|$\frac{1}{t} f \left(t\right)$|$\int_{s}^{\infty} F \left(𝜎\right) d 𝜎$|
|t Derivative|$f^{\left(\right. n \left.\right)} \left(t\right)$|$s^{n} F \left(s\right) - \sum_{k = 1}^{n} s^{n - k} f^{\left(\right. k - 1 \left.\right)} \left(0^{-}\right)$|
|t Integration|$\int_{0}^{t} f \left(𝜏\right) d 𝜏 = \left(u * f\right) \left(t\right)$|$\frac{1}{s} F \left(s\right)$|
|Convolution|$\left(f * g\right) \left(t\right) = \int_{0}^{t} f \left(𝜏\right) g \left(t - 𝜏\right) d 𝜏$|$F \left(s\right) \cdot G \left(s\right)$|
 
- Initial Value Theorem
	- $f \left(0^{+}\right) = \underset{s \rightarrow \infty}{l i m} ⁡ s F \left(s\right)$
- Final Value Theorem
	- $f \left(\infty\right) = \underset{s \rightarrow 0}{l i m} ⁡ s F \left(s\right)$
	- Where all poles of  
		are in the left half-plane
	- _Steady State Value_ 
$f \left(0^{+}\right) = \underset{s \rightarrow \infty}{l i m} ⁡ s F \left(s\right)$ $f \left(\infty\right) = \underset{s \rightarrow 0}{l i m} ⁡ s F \left(s\right)$
