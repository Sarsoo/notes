- Stochastic
- Recurrent structure
- Binary operation (+/- 1)
- Energy function

$$E=-\frac 1 2 \sum_j\sum_k w_{kj}x_kx_j$$
- $j\neq k$
- No self-feedback
- $x$ = neuron state
- Neurons randomly flip from $x$ to $-x$

$$P(x_k \rightarrow-x_k)=\frac 1 {1+e^{\frac{-\Delta E_k}{T}}}$$

- Energy change based on pseudo-temperature
	- System will reach thermal equilibrium
- Delta E is the energy change resulting from the flip
- Visible and hidden neurons
	- Visible act as interface between network and environment
	- Hidden always operate freely

# Operation Modes
- Clamped
	- Visible neurons are clamped onto specific states determined by environment
- Free-running
	- All neurons able to operate freely
- $\rho_{kj}^+$ = Correlation between states while clamped
- $\rho_{kj}^-$ = Correlation between states while free
- Both exist between +/- 1

$$\Delta w_{kj}=\eta(\rho_{kj}^+-\rho_{kj}^-), \space j\neq k$$