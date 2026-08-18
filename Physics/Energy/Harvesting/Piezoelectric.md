---
onenote-id: 0-4c5b32ed7977071f1d643bfc33a2849c!1-D084F068F621FF9!3720
---
# Stress  

- Tensile
	- Stretch
	- $𝜎$
	- Force per unit area
- Compressive
	- Squeeze

$𝜎$

# Strain  

- Tensile
	- Percentage change in length

Polarisation
 $\overset{\rightarrow}{P} = \epsilon_{0} 𝜒 \overset{\rightarrow}{E}$

- Polarising a dielectric using an electric field
 $P = d_{i j k} 𝜎_{j k} + 𝜇_{i j k l} \frac{𝜕 𝜖_{j k}}{𝜕 x_{l}}$  

- First term
	- Piezoelectric effect
		- Function of stress  
            
- Second term
	- Strain gradient
	- Flexoelectric effect
	- $𝜖$ for strain
 
- Less focus on flexoelectric, more piezo

Piezoelectric Effect
 
# Direct

$P = d 𝜎$

- Mechanical deformation polarises material
	- Voltage produced

# Converse

$𝜖 = d E$

- Voltage causes mechanical deformation

Crystallographic Point Groups
 
- Symmetric structures in unit cells
 
# Groups

- Centrosymmetric (11 groups)
	- Non piezo
- Non-Centrosymmetric (21 groups)
	- Piezoelectric (20 groups)
		- Pyroelectric (10 groups)
			- Spontaneous polarisation under heat
			- Ferroelectric
			- Non-ferroelectric
		- Non-pyroelectric (10 groups)
	- Non-piezoelectric (1 groups)

Poling
 
- Polarising by applying voltage  ![I Poling Voltage poling Axis NO Voltage Voltage Ap...](../../../img/OneNote/Piezoelectric%20image%20e786c449851a9e55.png)  
![a random orientation of polar domains prior polari...](../../../img/OneNote/Piezoelectric%20image%20daf77e0dc0c3614b.png)

Directions
 ![Poling](../../../img/OneNote/Piezoelectric%20image%209016f9d332d70a1c.png)

- 1, 2, 3, correspond to $x ,   y ,   z$
- 3 is set to polling direction
- Shear
	- Similar to rotation
		- Anti-clockwise = positive
		- Clockwise = negative
	- 4, 5, 6 for rotation around 1, 2, 3

Notation
 
- Superscript
	- T
		- Constant stress
			- Mechanically free
		- Direct effect
	- E
		- Constant field
			- Short circuit
		- Converse
	- D
		- Constant electrical displacement
			- Open circuit
		- Converse
	- S
		- Constant strain
			- Mechanically clamped
		- Direct effect
- Subscript
	- 2 subscripts
	- 1st
		- Direction of electric effect
	- 2nd
		- Direction of mechanical effect
 ![d33 Applied stress, or piezoelectrically induced s...](../../../img/OneNote/Piezoelectric%20image%2092409de6d873d62e.png)     

Quasi-DC Design
 $E n e r g y   h a r v e s t e d = \frac{1}{2} F \cdot x = \frac{1}{2} s_{33}^{E} \cdot \frac{F^{2} L}{A}$  
$k_{33}^{2} = \frac{E l e c .   E n e r g y}{M e c h .   E n e r g y} ,   k_{33} = \frac{d_{33}}{\sqrt{s_{33} \epsilon_{3}}}$  
![PIEZOELECTRIC DEVICE](../../../img/OneNote/Piezoelectric%20image%2085bb1afae40f5a00.png)

- Quasi-DC if frequency of motion is low (walking)
 
# AC design

- Use transducer to increase frequency of walking

Vibrations
 
- Q factor
	- Quality
- Amplitude of motion
- Model vibrations as sin waves
 
|   |   |
|---|---|
|![Exported image](../../../img/OneNote/Piezoelectric%20image%20d8c2abecfef8796d.png)|![Amplitude dB Center Frequency](../../../img/OneNote/Piezoelectric%20image%200d2cdd16fcd7b076.png)|
 $Q_{M} = \frac{F_{r}}{\left|F_{1} - F_{2}\right|}$  
$Q = \frac{f_{r}}{\Delta f} = 2 \pi \frac{e n e r g y   s t o r e d}{e n e r g y   d i s s i p a t e d}$  

- $f_{r}$ is resonant frequency
	- Q = resonance over difference between frequencies for amplitude to decrease by 3 dB
	- Q as high as possible
 
|   |   |
|---|---|
|![10 Q 10 Q 0.707 Q05 0.1 ff3dB Frequency, f](../../../img/OneNote/Piezoelectric%20image%20819efd1fbaa49882.png)|![8 8 R 0 90 uap!JJ3](../../../img/OneNote/Piezoelectric%20image%209a5d7202ccdf3926.png)|
 
- For high power
	- Increase size of components
	- Heavy components
	- High resonant frequencies
- However
	- Small things resonate at higher frequencies
	- Larger amplitude vibrations found at lower frequencies
	- Most systems emit range of frequencies
		- Bandwidth must be narrow to achieve high power
 
|   |   |
|---|---|
|![low frequency high frequency high amplitude low am...](../../../img/OneNote/Piezoelectric%20image%20ccac2285385fecd5.png)|![12 10 8 6 4 2 heel tapper 2 car inside car engine ...](../../../img/OneNote/Piezoelectric%20image%20df5977910fd7c385.png)|
 $P o w e r \propto \frac{m Y^{2} f^{3}}{𝜁}$  

- $m$ = Mass
- $Y$ = Amplitude
- $f$ = Frequency
- $𝜁$ = Damping (losses)
 
Vibration Modes
 
- Longitudinal
- Transverse
 ![Symmetric Lamb Wave AntiSymmetric Lamb Wave](../../../img/OneNote/Piezoelectric%20image%20259f0872af3e2775.png)  
![Machine generated alternative text _ _z4 Rayleigh](../../../img/OneNote/Piezoelectric%20image%208270768b6a783d97.png)

- Rotation action
 ![Machine generated alternative text Love](../../../img/OneNote/Piezoelectric%20image%20b40ba16715cef61b.png)

- Shear-like action

Design
 ![Machine generated alternative text bimorph Vin mul...](../../../img/OneNote/Piezoelectric%20image%20bc6c5ef5fbe40f03.png)  

- Bimorph
	- Arm attached to a wall
		- Cantilever
	- Two piezoelectric elements either side of a skeleton substructure
	- Neutral plane
		- Plane of device that doesn't change dimensions
		- Central plane of cantilever
			- Above will stretch
			- Below squeezes
- Multilayer
	- Interleaved structure of electrodes from either side
	- Piezoelectric materials in-between
 ![Machine generated alternative text Moonie a b Cymb...](../../../img/OneNote/Piezoelectric%20image%20372263f94b9b21f6.png)

![Machine generated alternative text 3 2 THckJEss mo...](../../../img/OneNote/Piezoelectric%20image%20978fddb656c590e2.png)

Nano Piezotronics
 
- Allows wider device concepts
- More shapes/morphologies
- Surface becomes more important
- Can be fabricated at low temperatures with less toxic materials
 
# ZnO

- Wide band gap semiconductor
	- 3.3 eV
- Zinc Oxide has low exciton binding energy
	- 60 meV
	- Exciton
		- Bound electron and hole
		- Usually generated under optical excitation
 
|   |   |
|---|---|
|![Exported image](../../../img/OneNote/Piezoelectric%20image%20e5cf0099e711c99e.png)<br><br># Wurtzite Structure|![Exported image](../../../img/OneNote/Piezoelectric%20image%20d36834f794e2ff9e.png)<br><br># Zinc-blend Structure|
 ![Exported image](../../../img/OneNote/Piezoelectric%20image%203f65408d83f2d6c5.png)  

- Different growth techniques and morphologies

|   |   |
|---|---|
|# Pros|# Cons|
|Simple|Lifetime issues|
|Direct mech to electrical conversion|High stiffness|
|No additional component required|High amplitude required|
|Good for micro and macro scale|Vibrations at low frequencies|
|No input voltage need||
|High voltage output||

|   |   |   |
|---|---|---|
|![Unstressed Crystal centres of symmetry and coincid...](../../../img/OneNote/Piezoelectric%20image%20e256c1afa0305d90.png)|![mpresse Crystal centre Of symmetry for negative ch...](../../../img/OneNote/Piezoelectric%20image%20cd16bf4bc4b3c9c8.png)|![Stretched Crystal centre of symmetry for positive ...](../../../img/OneNote/Piezoelectric%20image%2074efa348adf27c5a.png)|
 
- Moving charges moves average charges

Constants & Coefficients
 
# Piezoelectric

- d
	- C/N
	- Charge developed/applied stress
- g
	- Vm/N
	- Electric field developed/applied stress
- h
	- m/V
	- Strain developed/applied E-field
- e
	- N/Vm
	- Stress developed/applied E-field
 
# Electromechanical Coupling

$k$

- $k$
- Parameter to compare different piezoelectric materials
- Measure of interchange between electrical and mechanical energy