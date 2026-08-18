---
onenote-id: 0-b3dee464f14f09b6156b7e484187453b!1-D084F068F621FF9!3720
---
# Equilibrium
- Without EM field
	- Electrons have random thermal motion
		- $v_{t h}$
			- Can be 106 m/s
	- No net current
- Average K.E. of electron in 3D conduction band is $3 / 2 k T$
	- Law of equipartition of energy
- 2D
	- $k T$
- 1D
	- $1 / 2 k T$
- Each dimension gets extra half

$v_{t h}$ $1 / 2 k T$  
$$\frac{3}{2} k T = \frac{1}{2} m v_{t h}^{2}$$ 
$$v_{t h} = \sqrt{\frac{3 k T}{m}} = \sqrt{\frac{3 \cdot 1 . 38 \times 10^{- 23} \cdot 300}{0 . 067 \cdot 9 . 11 \times 10^{- 31}}} = 0 . 45 \times 10^{6}   m / s$$  

## Out of Equilibrium

- Acquires drift velocity $v_{d}$
	- Smaller than thermal velocity
- $\underset{\underline}{J} = - n e \underset{\underline}{v_{d}}$
	- $n$ is the carrier density
	- Negative is for conventional current

$\underset{\underline}{J} = - n e \underset{\underline}{v_{d}}$  
$\left⟨v\right⟩ = \left⟨v_{0}\right⟩ - \frac{e E t}{m} = \frac{- e E 𝜏_{c}}{m}$

- Similar to Newton's second law
	- Random scattering implies V0 = 0
 $$J = - n e v_{d} = \frac{n e^{2} 𝜏_{c}}{m} E$$ 
 $$J = 𝜎 E$$

- Advanced ohm's law

$$𝜎 = \frac{n e^{2} 𝜏_{c}}{m} = n e 𝜇$$

- Increase carrier concentration to increase conductivity
- More impurity scattering which also lowers
 $$l_{c} = 𝜏_{c} v_{d}$$

- Mean free path
 
- For effective mass $m \star$
	- Momentum is $m \star \cdot v_{d}$
	- Apply Newton's second
		- Rate of change of momentum to force experienced in  
            
	- $\frac{m^{*} \underset{\underline}{v_{d}}}{𝜏_{c}} = q \underset{\underline}{E}$
- Mobility is drift velocity per unit electric field

$\frac{m^{*} \underset{\underline}{v_{d}}}{𝜏_{c}} = q \underset{\underline}{E}$  

|   |   |
|---|---|
|$𝜇 = \frac{v_{d}}{E}$|$𝜇 = \frac{e 𝜏_{c}}{m^{*}}$|

![IE7 IE6 IE2 T300 K IE5 Electric field Vcm](../../img/OneNote/Carrier%20Transport%20image%209ba7784a709a5c5a.png)

# AC Conductivity
 $$E \left(t\right) = R e \left(E \left(𝜔\right) e^{j 𝜔 t}\right)$$  
$$J \left(t\right) = R e \left(J \left(𝜔\right) e^{j 𝜔 t}\right)$$  
$$J \left(𝜔\right) = 𝜎 \left(𝜔\right) E \left(𝜔\right)$$

| $𝜎 \left(𝜔\right) = \frac{𝜎_{0}}{1 + j 𝜔 𝜏}$ | $𝜎 \left(𝜔\right) = \frac{𝜎_{0}}{1 - i 𝜔 𝜏}$ |
| :-----------------------------------------------: | :-----------------------------------------------: |

Where $j = - i$
 $$𝜎_{0} = \frac{n e^{2} 𝜏}{m}$$

- $𝜎_{0}$ is the DC conductivity
 $$𝜎 \left(𝜔\right) = \frac{𝜎_{0}}{1 + j 𝜔 𝜏} \times \frac{1 - j 𝜔 𝜏}{1 - j 𝜔 𝜏} = \frac{𝜎_{0} - j 𝜎_{0} 𝜔 𝜏}{1 + 𝜔^{2} 𝜏^{2}}$$  
$$𝜎_{1} = \frac{𝜎_{0}}{1 + 𝜔^{2} 𝜏^{2}}$$  
$$𝜎_{2} = \frac{- 𝜎_{0} 𝜔 𝜏}{1 + 𝜔^{2} 𝜏^{2}}$$  
![LOW frequency limit O, O then 51 and 02 O High fre...](../../img/OneNote/Carrier%20Transport%20image%20fa03815315062eb8.png)  

![1.0 0.8 Ima 0.6 0.4 0.2 0.0 loge](../../img/OneNote/Carrier%20Transport%20image%2046396bbef07f6dbb.png)

![Resistivity of Metals with Temperature and impurit...](../../img/OneNote/Carrier%20Transport%20image%20928db7327f66edf6.png)  

- Resistivity of metal increases
	- Linearly with temp
	- Lattice atoms oscillate about equilibrium
	- Increases incoherent scattering
		- Number of electron-atom collisions
- Residual resistivity, $𝜌_{r e s}$
	- Imperfections in the crystal
		- Impurities
		- Vacancies
		- Grain boundaries
		- Dislocations
	- Basically not temperature-dependent
- Small additions cause linear shift in resistivity
	- Atoms of different size cause variation in lattice parameter
		- Thus in electron scattering
	- Atoms have different valences
		- Local charge difference
			- Higher scattering probability
	- Impurities with different electron concentration
		- Alters position of Fermi energy

# High E
 ![GaAs 3.0 IS 1.0 Si 10 20 InP 30 40 50 ELECTRIC FIE...](../../img/OneNote/Carrier%20Transport%20image%20e26f87d21c2b7e2f.png)  
![CCNOuCTON VALENCE 0](../../img/OneNote/Carrier%20Transport%20image%20fdde4e88da270650.png)

- Start populating higher bands
	- Less curved
	- Higher effective mass
	- Lower mobility
 
$$𝜎 = n e 𝜇$$
