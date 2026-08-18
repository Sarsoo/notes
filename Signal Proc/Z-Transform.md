---
onenote-id: 0-2e29503afd8c465a86e52a5e86aec2f7!1-D084F068F621FF9!3691
---
Converts discrete-time signal to complex frequency-domain

- Laplace equivalent for discrete signals
- Generalisation of the discrete-time Fourier transform
	- $X(\omega)=\sum\limits_{-\infty}^{\infty}x\left[n\right]e^{-j\omega n}$
	- With $z = e^{j 𝜔}$

$x \left[n\right] \leftrightarrow X \left(z\right)$  

- Bilateral
	- $\mathcal{Z} \{x \left[n\right]\} = X (z) = \sum\limits_{n = - \infty}^{\infty} x \left[n\right] z^{- n}$
- Unilateral
	- $\mathcal{Z} \left{x \left[n\right]\right} = X \left(z\right) = \sum_{n = 0}^{\infty} x \left[n\right] z^{- n}$
- $z = A e^{j \phi} = A \cdot \left(c o s ⁡ \phi + j s i n ⁡ \phi\right)$
	- _A = magnitude_
	- $\phi$ _= complex argument, (phase)_

$\mathcal{Z} \left{x \left[n\right]\right} = X \left(z\right) = \sum_{n = - \infty}^{\infty} x \left[n\right] z^{- n}$ $\mathcal{Z} \left{x \left[n\right]\right} = X \left(z\right) = \sum_{n = 0}^{\infty} x \left[n\right] z^{- n}$ $z = A e^{j \phi} = A \cdot \left(c o s ⁡ \phi + j s i n ⁡ \phi\right)$  

- Inverse
	- $\left(x \left[n\right] = \mathcal{Z}\right)^{- 1} \left{X \left(z\right)\right} = \frac{1}{2 \pi j} \oint X \left(z\right) z^{n - 1} d z$
	- _Over C where C is a counter clockwise closed path encircling origin and ROC_
		- _Encircles all poles of_ $X \left(z\right)$

$\left(x \left[n\right] = \mathcal{Z}\right)^{- 1} \left{X \left(z\right)\right} = \frac{1}{2 \pi j} \oint X \left(z\right) z^{n - 1} d z$
  
|   |   |   |
|---|---|---|
||_t_|_z_|
|Linearity|$a f \left[n\right] + b g \left[n\right]$|$a F \left(z\right) + b G \left(z\right)$|
|t Delay|$f \left[n - k\right]$|$z^{- k} F \left(z\right)$|
|t Reversal|$f \left[- n\right]$|$F \left(z^{- 1}\right)$|
|t scale|$f \left[n/k\right]$|$F \left(z^{k}\right)$|
|z Scaling|$a^{n} f \left[n\right]$|$F \left(a^{- 1} z\right)$|
 
- Initial Value Theorem
	- $f \left[0\right] = \underset{z \rightarrow \infty}{l i m} ⁡ F \left(z\right)$
	- If $f \left[n\right]$ is causal
- Final Value Theorem
	- $f \left[\infty\right] = \underset{z \rightarrow 1}{l i m} ⁡ \left(z - 1\right) F \left(z\right)$
	- If the poles of (z−1)X(z) are inside the unit circle

$f \left[0\right] = \underset{z \rightarrow \infty}{l i m} ⁡ F \left(z\right)$ $f \left[\infty\right] = \underset{z \rightarrow 1}{l i m} ⁡ \left(z - 1\right) F \left(z\right)$

$H \left(z\right) = \frac{Y \left(z\right)}{X \left(z\right)} = \frac{S \left(z\right)}{U \left(z\right)}$

Unit Circle
 
- Because of relationship with DTFT
	- $z = e^{j 𝜔}$
	- Defines a unit circle on the  
		plane
	- DTFT only defined on the circle

$z = e^{j 𝜔}$

![Example 2 Let, yn 1, then an z This is a geometric...](../../img/OneNote/Z-Transform%20image%206adb4230d5d1ce2d.png)  

- Infinite geometric series

[Getmyuni - z-transform](https://getmyuni.azureedge.net/assets/main/study-material/notes/electronics-communication_engineering_digital-signal-processing_the-z-transform_notes.pdf)  
[https://www.dip.ee.uct.ac.za/~nicolls/lectures/eee4114f/03_ztrans.pdf](https://www.dip.ee.uct.ac.za/~nicolls/lectures/eee4114f/03_ztrans.pdf)

![1 2 3 4 5 6 7 9 10 Signal, xn n nanun coswon un an...](../../img/OneNote/Z-Transform%20image%201f63db80528689ce.png)

![Exported image](../../img/OneNote/Z-Transform%20image%2099c907130d3109b4.png)  

- Top causal
- Bottom anti-causal