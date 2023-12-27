---
tags:
  - signals
---
$$Y(s)=H(s)\cdot X(s)$$
- $H(s)=\frac{Y(s)}{X(s)}=\frac{\mathcal L\{y(t)\}}{\mathcal L\{x(t)\}}$

$$Y(z)=H(z)\cdot X(z)$$
- $H(z)=\frac{Y(z)}{X(z)}=\frac{\mathcal Z\{y[n]\}}{\mathcal Z\{x[n]\}}$

$$G(\omega)=\frac{|Y|}{|X|}=|H(j\omega)|$$
- $H(j\omega)$, Frequency response

$$\phi(\omega)=arg(Y)-arg(X)=arg\left(H\left(j\omega\right)\right)$$
- $\phi(\omega)$, Phase shift

$$\tau_\phi(\omega)=-\frac{\phi(\omega)}{\omega}$$
- $\tau_\phi$, Phase delay
- Frequency-dependent amount of delay introduced to the sinusoid by $H$

$$\tau_g(\omega)=-\frac{d\phi(\omega)}{d\omega}$$
- $\tau_g$, Group delay
- Frequency-dependent amount of delay introduced to the envelope of the sinusoid by $H$

[Partial Fractions](https://lpsa.swarthmore.edu/BackGround/PartialFraction/PartialFraction.html#Order_of_numerator_polynomial_is_not_less_than_that_of_the_denominator)
[Partial Fractions for Laplace](https://lpsa.swarthmore.edu/LaplaceXform/InvLaplace/InvLaplaceXformPFE.html)
[Inverse Z Transform](https://lpsa.swarthmore.edu/ZXform/InvZXform/InvZXform.html)

[Discrete Time Systems:Impulse responses and convolution; An introduction to the Z-transform](https://homes.esat.kuleuven.be/~maapc/static/files/SYSTHEORY/Slides/Lecture5/Lecture5-Impulse%20responses%20and%20convolution%20layout.pdf)