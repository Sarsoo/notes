---
onenote-id: 0-804f950a11dc0a92058f9c14c224e886!1-D084F068F621FF9!3720
---
Conductance

# 3D

$G = \frac{𝜎 A}{L}$  

- S/m

# 2D

$G = \frac{𝜎 W}{L}$  

- S

- Diffusive
	- Elastic mean free path is shorter than device length
	- $T < 1$
- Ballistic
	- No scattering
	- $T = 1$
- Quantum ballistic
	- So short that quantum nature relevant
	- De Broglie

$T < 1$ $T = 1$  
![Exported image](../../img/OneNote/Mesoscopic%20image%2010ee6c4eb221d21a.png)

Quantum Point Contact
 
- Conductance is quantised in units of $\left(e^{2}\right)/h$
	- Typically 2 x
		- Spin degeneracy
	- Doesn't depend on material parameters
		- Effective mass
 
# Split Gate

- Apply negative voltage to gate
	- Repels electrons
	- Squeezes electrostatic potential
	- Makes channel so small it only allows a small number of electrons
- Electrodes don't move
 ![AIGaAs 000 GaAs conducting 2DEG](../../img/OneNote/Mesoscopic%20image%2021a94db14bbbf5b2.png)  
![G in units of 2e2h G 2811 Il](../../img/OneNote/Mesoscopic%20image%202f44bba1ff141ffb.png)

- Low temperature

$\left(\left(2 e\right)^{2}\right)/h$ Quantised Conductance
 
- Ballistic
	- Ignore scattering
- $J = n e v$
	- For 3D
- $J = n e v_{f}$
	- For 1D
	- Fermi velocity
	- N = carriers per unit length
	- m-1 x C x ms-1 = C/s
		- Current not current density
- Replace carrier density with DOS x Energy interval
- Turn velocity to momentum
	- $\hbar \cdot k_{F} = m^{*} \cdot v_{F}$

$J = n e v$ $J = n e v_{f}$ $\hbar \cdot k_{F} = m^{*} \cdot v_{F}$ $I = n e v_{F} = \left(D O S \cdot d E\right) \cdot e \cdot \frac{\hbar k_{F}}{m^{*}}$

- Need DOS dE for 1D
	- $D O S = \frac{d k}{\pi}$
	- Is a  
		- Not helpful
		- Change to energy with [E-k relation](E-k%20%20Bloch)

$D O S = \frac{d k}{\pi}$  
$\frac{d k}{\pi} = \frac{1}{\pi} \frac{m^{*}}{\hbar^{2} k_{F}}   d E$  
$I = \frac{1}{\pi} \frac{m^{*}}{\hbar^{2} k_{F}}   \cdot d E \cdot e \cdot \frac{\hbar k_{F}}{m^{*}}$  
$I = \frac{1}{\pi} \frac{d E \cdot e}{\hbar} = \frac{2 e   d V \cdot e}{h} = \frac{2 e^{2}}{h}   d V$  

- Go from energy range to voltage range using
	- $d E = e   d V$

$d E = e   d V$  
$G_{0} = 7 . 75 \times 10^{- 5}   \Omega^{- 1} \approx \left(12 . 9   k \Omega\right)^{- 1}$  

- For electrons/holes
 
# Conclusions

- Conductance is quantised in units of above
	- Factor of 2 from spin degeneracy
- Resistance quantised in units of $\frac{h}{2 e^{2}} = 12 . 9   k \Omega$
	- Quantum of resistance
	- $R_{Q}$
- Graphene has valleys at K and K'
	- Each has a channel for conduction
	- Doubles conductance
	- $\left(6 . 5   k \Omega\right)^{- 1}$

$R_{Q}$ $\left(6 . 5   k \Omega\right)^{- 1}$  
$g_{v} \cdot g_{s} \cdot \frac{e^{2}}{h}$  

- Where $g_{v}$ is valley degeneracy
- Where $g_{s}$ is spin degeneracy
 $G = \frac{2 e^{2}}{h} M$  

- To scale by number of modes
	- gs = 2
 
# Where From?

- Large contacts
	- Reservoirs of charge
- Contact resistance
	- Electron crowding as many modes are coupled to 1
 
# Calculating Modes

$M = i n t \left(\frac{W}{\left(\lambda_{F}\right)/2}\right)$

- W = Device width
- $\lambda_{F}$ = Fermi wavelength
 $\lambda_{F} = \sqrt{\frac{2 \pi}{n_{s}}}$

- $n_{s}$ is carrier density

Scattering
 ![Exported image](../../img/OneNote/Mesoscopic%20image%2024bc857fb7bfd32b.png)  
$T_{12} = T_{1} T_{2} \left(1 + R_{1} R_{2} + \left(R_{1} R_{2}\right)^{2} + \ldots\right)$  

- Constantly decreasing as R \< 1
	- Use infinite sum
 $T_{12} = \frac{T_{1} T_{2}}{1 - R_{1} R_{2}}$  

# Multiple Scattering

$\frac{1 - T_{12}}{T_{12}} = \frac{1 - T_{1}}{T_{1}} + \frac{1 - T_{2}}{T_{2}}$  
$\frac{1 - T \left(N\right)}{T \left(N\right)} = N \frac{1 - T}{T}$  

- For N scattering centres of the same T
 $T \left(N\right) = \frac{T}{N \left(1 - T\right) + T}$  

- Transmission coefficient in terms of number of centres
- Want in terms of scatters per unit length,  
    
- $N = v L$

$N = v L$  

$T \left(L\right) = \frac{T/\left(v \left(1 - T\right)\right)}{L + T/\left(v \left(1 - T\right)\right)}$
 $L_{0} = \frac{T}{v \left(\right. 1 - T \left.\right)}$

- Mean free path
 $T \left(L\right) = \frac{L_{0}}{L + L_{0}}$  

- Transmission coefficient in terms of length
- Interpret L0 as the mean free path
- L \>\> L0, T-\> 0
	- Diffusive transport
- L \<\< L0, T-\> 1
	- Ballistic conduction

Landauer Formalism
 
- Calculating conductance from transmission coefficient and number of modes
 
# Incoherent Scattering

$G = \frac{2 e^{2}}{h} M T$

- For conductance
 $R = \frac{R_{Q}}{M T}$  

- M = Modes
- T = Transmission coefficient
 ![0.05x 0.05 i Including multiple reflections T12 TI...](../../img/OneNote/Mesoscopic%20image%202430f9df4795524e.png)  

# Contact/Device Terms

$R_{t o t a l} = \frac{h}{2 e^{2} M} \frac{1}{T} = \frac{h}{2 e^{2} M} + \frac{h}{2 e^{2} M} \frac{1 - T}{T}$  
$\frac{1}{T} = 1 + \frac{1 - T}{T}$

- $\frac{1}{T} = 1 + \frac{1 - T}{T}$
- 2 Terms
	- First only dependent on modes
		- Contact term
	- Second dependent on modes and transmission
		- Device term
 $R_{d e v i c e} = \frac{h}{2 e^{2} M} \frac{1 - T}{T} = \frac{h}{2 e^{2} M} \frac{\left(1 - \frac{L_{0}}{L + L_{0}}\right)}{\frac{L_{0}}{L + L_{0}}}$  
$R_{d e v i c e} = \frac{h}{2 e^{2} M} \left(\frac{L}{L_{0}}\right)$  

# Resistance increases as length increases

- # Resistance increases as length increases
    
	- Ohm's law
 ![Resistance of diffusive conductor as a function of...](../../img/OneNote/Mesoscopic%20image%20cb283384117a3420.png)

# Does not tend to 0

- # Does not tend to 0
    
	- Finite contact resistance
 $R \left(L\right) = \frac{h}{2 e^{2} M} + \frac{h}{2 e^{2} M} \frac{L}{L^{0}}$  
$R \left(L\right) = \frac{R_{Q}}{M} + \frac{R_{Q}}{M} \frac{L}{L_{0}}$  

- RQ = 12.9k
- First term is a  
	intercept
- Second term depends on L
	- Gradient term
 
# Coherent Scattering

- Electron acquires phase shift after each scattering event
- Phase-coherence length, $L_{\varphi}$
	- Measure of distance that electron propagates in-phase
	- Phase-relaxation length
	- No classical analogue
	- Wavefunction has a phase
- Phase-relaxation time, $t_{\varphi}$
- Low temperatures
	- Phase-coherence length can be longer than elastic mean free path
	- Number of elastic scattering events occur before phase information lost
	- Phase not lost at elastic scattering event
		- Shifted by well-defined amount
 $T_{12} = \frac{T_{1} T_{2}}{1 + R_{1} R_{2} - 2 \sqrt{R_{1} R_{2}} c o s ⁡ 2 𝜃}$  

- Maximises for  
	- In phase with confined energy levels of quantum well
	- $T_{12} = 1$
	- Can get full transmission at certain energies

$T_{12} = 1$

Current
 ![Exported image](../../img/OneNote/Mesoscopic%20image%2008709732b15712bc.png)  

- $𝜇$ for electrochemical potentials/energy level
- Channel of molecules/graphene/semiconductor
- Are there states in the channel to allow conduction from source to drain
	- Even when source and drain are biased
 ![Pli chnner qVD k12](../../img/OneNote/Mesoscopic%20image%203204f25cd1302cb7.png)

- Increasing voltage
	- Decreases drain potential
	- How does channel energy move with drain voltage
 $V_{L} = \frac{C_{S} V_{S} + C_{D} V_{D} + C_{G} V_{G}}{C_{S} + C_{D} + C_{G}}$  

- Laplace potential
	- Potential of the channel
- Weighted average of voltages by capacitances
 
# Weak Gate Coupling

- Cg = 0
- VL is proportional to VD
	- For matched source/drain capacitance = 1/2
	- Not ideal for transistor
 $V_{L} = \frac{C_{D} V_{D}}{C_{S} + C_{D}}$  

# Strong Gate Coupling

- For CG dominance
	- VL=VG
- Thin layer
- High dielectric material
 $V_{L} = \frac{C_{S} V_{S} + C_{D} V_{D} + C_{G} V_{G}}{C_{S} + C_{D} + C_{G}} \approx \frac{C_{G} V_{G}}{C_{S} + C_{D} + C_{G}} \approx \frac{C_{G}}{C_{S} + C_{D} + C_{G}} V_{G}$  

- Assumes that a channel has formed
	- Voltage is above threshold
	- $V_{L} = V_{G} - V_{t h}$
- $U_{L} = q V_{L}$
	- Channel potential energy

$V_{L} = V_{G} - V_{t h}$ $U_{L} = q V_{L}$

![source Increasing gate voltage 15 position drain 1...](../../img/OneNote/Mesoscopic%20image%20c18e388c455a482f.png)

Current Coupling
 
- Current flows comes from coupling between contacts and electron energy levels
	-   
		is the current coupling coefficient
- Current flows from contact to channel to contact
- $\frac{𝛾}{\hbar}$
	- J/Js = s-1
	- Rate of electron escape at each contact
 
If $𝛾 = 1   m e V$ then $\frac{𝛾}{\hbar} = \frac{10^{- 3} \cdot 1 . 6 \times 10^{- 19}}{1 . 054 \times 10^{- 34}} = 10^{12}   s^{- 1}$
 
- Pico-seconds to escape source or drain contact
	- Increasing voltage increases current
		- Reduces time to escape contacts
 
# Analysis
 
- $E$ is an energy level between $𝜇_{1}$ and $𝜇_{2}$
- $N$ is the average occupancy of the level at steady state
	- Between 0 and 1
- $f$ is Fermi-Dirac occupancy
 
|   |   |
|---|---|
|$I_{1} = q \left(f_{1} - N\right) \frac{𝛾_{1}}{\hbar}$|$I_{2} = q \left(N - f_{2}\right) \frac{𝛾_{2}}{\hbar}$|

- Source and drain currents
	- Set equal
- $f_{1} - N$ is net occupancy of the source - channel
- $N - f_{2}$ is net occupancy of channel - drain
 $q \left(f_{1} - N\right) \frac{𝛾_{1}}{\hbar} = q \left(N - f_{2}\right) \frac{𝛾_{2}}{\hbar}$  
$N = \frac{f_{1} 𝛾_{1} + f_{2} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}}$  
$I_{1} + I_{2} = \frac{q}{\hbar} \left(𝛾_{1} f_{1} - 𝛾_{1} N + 𝛾_{2} N - 𝛾_{2} f_{2}\right)$  
$I_{1} = \frac{q}{\hbar} \cdot \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}} \cdot \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)$  
$I = \frac{2 q}{\hbar} \cdot \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}} \cdot \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)$  

- Above for spin degeneracy
- Need strong coupling for current
- No current when f1 = f2
- Multiple suitable energy levels can be used for conduction
 
# Voltage

- Relate $f_{1} - f_{2}$ to voltage
- Define $E_{F}$ which is same as $𝜇$ at equilibrium
- Apply voltage to drain
	- $𝜇_{1} = E_{F}$
	- $𝜇_{2} = E_{F} - e V_{D}$
	- Shift so $𝜇_{1}$ is plus $\frac{1}{2}   e V_{d}$ , $𝜇_{2}$ is minus $\frac{1}{2}   e V_{d}$

$𝜇_{1} = E_{F}$ $𝜇_{2} = E_{F} - e V_{D}$  
$f \left(E\right) = f \left(E_{F}\right) + \frac{d f}{d E} \left(E - E_{F}\right)$  
$f_{1} \left(E - 𝜇_{1}\right) = f \left(E_{F}\right) + \frac{d f}{d E} \left(E - 𝜇_{1} - E_{F}\right)$  
$f_{2} \left(E - 𝜇_{2}\right) = f \left(E_{F}\right) + \frac{d f}{d E} \left(E - 𝜇_{2} - E_{F}\right)$  
$f_{1} \left(E\right) - f_{2} \left(E\right) = \frac{d f}{d E} \left(E - 𝜇_{1} - E_{F} - E + 𝜇_{2} + E_{F}\right)$  
$f_{1} \left(E\right) - f_{2} \left(E\right) = \frac{d f}{d E} \left(𝜇_{2} - 𝜇_{1}\right) = - e V_{D} \frac{d f}{d E}$  
![We now need an expression for In general fE exp 1 ...](../../img/OneNote/Mesoscopic%20image%20688cf54e5680b56f.png)  
$I = V_{D} \frac{e^{2}}{\hbar} \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}} \frac{1}{4 k T}$  

- What is $\frac{d f}{d E}$ when $E = 𝜇$
	- Spread in energy of the Fermi function
	- Corresponding spread in voltage is 4kT/e
 $\frac{\Delta I}{\Delta V} = \frac{\left(e 𝛾\right)/\left(2 \hbar\right)}{\left(4 k T\right)/e}$  

- As  
	,  
	- Quantised in units of $\left(e^{2}\right)/h$
- Assumes a single sharp energy level
	- Not isolated but connected to contacts
		- Origin of escape time
 $\Delta V = \frac{2 𝛾 + 4 k T}{e}$  
$\frac{\Delta I}{\Delta V} = \frac{\left(e 𝛾\right)/\left(2 \hbar\right)}{\left(\left(2 𝛾 + 4 k T\right)\right)/e}$

Single Level To DOS
 ![Source Drain](../../img/OneNote/Mesoscopic%20image%207024c6d05b9dde22.png)  

$I = \frac{2 q}{\hbar}   \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}} \int_{- \infty}^{\infty} D \left(E\right)   d E   \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)$
 
$I = \frac{2 q}{h} \int_{- \infty}^{\infty} 2 \pi   \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}}   D \left(E\right)   d E   \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)$
 
$I = \frac{2 q}{h} \int_{- \infty}^{\infty} T \left(E\right)   d E   \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)$
 $T \left(E\right) = 2 \pi \frac{𝛾_{1} 𝛾_{2}}{𝛾_{1} + 𝛾_{2}}   D \left(E\right)$  

- Transmission coefficient
	- 0 for no density of states
		- Current of 0
	- Also depends on contact coupling

![VD potential applied to contact 2 0.6 0.5 0.4 0.3 ...](../../img/OneNote/Mesoscopic%20image%20f839c4396b58a8a8.png)

Resonant Tunnelling Diode
 ![Valence band ev Conduction band ev](../../img/OneNote/Mesoscopic%20image%20f2996f0142d21cf2.png)

- Tune the barrier height by varying the fraction of Al
 
- Transmission maximises when resonating with confined energy levels
- Higher energy levels have broader peaks as a result of uncertainty principle
	- Higher energy + lower potential barrier
	- ![Barrier height](../../img/OneNote/Mesoscopic%20image%2057f15f67095edaf2.png)
	- Reduced lifetime
		- Increases energy band
	- Quasi-bound
 
|   |   |
|---|---|
|![0.8 0.6 0.4 0.2 0.1 0.2 0.3 0.4 Electron energy eV...](../../img/OneNote/Mesoscopic%20image%204ca1ab2379c1c436.png)|![10 0.05 0.1 0.15 0.2 0.25 Electron energy eV 0.3](../../img/OneNote/Mesoscopic%20image%20d827b2549ac241db.png)|
 ![Exported image](../../img/OneNote/Mesoscopic%20image%20bfa4c4642367045a.png)  

- Von
	- First energy level in resonance with the fermi level of left contact
	- $E_{1} = E_{F L}$
		- $E_{F L}$ = Fermi level of left hand contact
- Voff
	- First energy level falls out of resonance with the fermi level of left contact
- Transmission curve often takes Lorentzian shape
- Negative differential resistance
	- c)
	- Slope of I-V is negative
	- Increasing voltage reduces current

$E_{1} = E_{F L}$  

$I = \frac{2 q}{h} \int_{- \infty}^{\infty} T \left(E\right) \left(f_{1} \left(E\right) - f_{2} \left(E\right)\right)   d E  $
 $I \approx \frac{2 e}{h} T_{p e a k} \int_{- \infty}^{\infty} \left[1 + \left(\frac{E - E_{p e a k}}{\left(\Gamma\right)/2}\right)^{2}\right]^{- 1}   d E$  

- $\left(\Gamma\right)/2$ = Half-width
 $I = \frac{2 e}{h} \frac{\pi}{2} \Gamma T_{p e a k}$  
$J = \frac{e}{4 \pi} \frac{m^{*}}{\hbar^{3}}   \left(E_{F l} - E_{n}\right) \Gamma_{n} T \left(E\right) ,     w h e n   E_{c , m i n} < E_{n} < E_{F L}$  

- $E_{n}$ = Confined energy level
- $\Gamma_{n}$ = Width of confined energy level
- RTD current density at low temperatures

Semiconductor Contacts
 
- Can dope fermi level past conduction band minimum
- Hard to do in silicon
	- Much easier in GaAs
		- Lower effective mass
- Degenerate semiconductor
	- Super high electron concentration
 ![2mnekT The effective density of states for GaAs is...](../../img/OneNote/Mesoscopic%20image%203702d673443f9c2d.png)  
![Electron concentration cm 3 1.00E16 1.OOE17 1.OOE1...](../../img/OneNote/Mesoscopic%20image%20abe13f26f2194301.png)  
 
![1112 q Io](../../img/OneNote/Mesoscopic%20image%207039e12fdfc510ba.png)  

- Only energy levels between $𝜇_{1}$ (source) and $𝜇_{2}$ (drain) contribute to the current
 ![1. Will current flow through level A? At an energy...](../../img/OneNote/Mesoscopic%20image%2018516fc3eed709e8.png)

