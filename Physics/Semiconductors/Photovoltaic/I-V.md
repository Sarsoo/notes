---
onenote-id: 0-5150bfcb059c069f18c5e784c9ccbf6c!1-D084F068F621FF9!3720
---
![1. No light Dark current v 2. With light Dark curr...](../../../img/OneNote/I-V%20image%2061fcf9f30014a857.png)  

- No light looks like diode

$I = I_{0} \left(e^{\left(q V\right)/\left(k T\right)} - 1\right)$ $I = I_{0} \left(e^{\left(q V\right)/\left(k T\right)} - 1\right) - I_{L}$

- $I_{0}$ = reverse saturation current
- Idealised
 
# Realistic

With parasitic losses

$I = I_{0} \left(e^{\left(q \left(V - R_{S} I\right)\right)/\left(k T\right)} - 1\right) - I_{L} + \frac{V - R_{S} I}{R_{S H}}$  
![Exported image](../../../img/OneNote/I-V%20image%20a4500c92ae03df75.png)

- $R_{S}$ = Series resistance
	- Ideally 0
	- Resistance to charge charrier transport through photoactive layer
	- Contact resistances
	- Transport through the contacts themselves
- $R_{S H}$ = Shunt resistance
	- Ideally infinity
	- Infinite for ideal diodes
	- Electrical shorting/leakage through the device
 ![Exported image](../../../img/OneNote/I-V%20image%2050818255660f5764.png)  
![Exported image](../../../img/OneNote/I-V%20image%205d7aaeb691f9f1dd.png)   
![Dark current 10 Light current IL llsc Light curren...](../../../img/OneNote/I-V%20image%20aae26bfc249cda26.png)  

- Voc = Open circuit voltage
	- Let I = 0 to solve
- Isc = Short circuit current
	- Maximum extractable current
	- When V = 0, Isc = IL

Power Rectangle
 ![sc Dark current Maximum power rectangle Light curr...](../../../img/OneNote/I-V%20image%200385482d2220f847.png)  

- Seek largest area / power (IV)
 $P_{m} = I_{m} V_{m}$  
$𝜂 = \frac{I_{m} V_{m}}{P_{s}}$

- Efficiency
	- Ps = Incident light power
 $F F = \frac{I_{m} V_{m}}{I_{s c} V_{o c}}$

- Fill factor
	- Ratio of ideal and actual I/V values
	- Want high
	- Measure of how square?
 $𝜂 = \frac{F F \cdot I_{s c} V_{o c}}{P_{s}}$

# Short-Circuit Current

- Absorb wide spectral range
- Dominated by generation rate and collection probability
- Improve with better photon management
 
# Open-Circuit Voltage

$V_{o c} < V_{b i} < \left(E_{g}\right)/q$

- $V_{o c} < V_{b i} < \left(E_{g}\right)/q$
- Large values
	- Large electric potential for carriers
- Improve with better materials
 
Increasing one tends to reduce the other

- Small band gaps reduce working voltages
	- From above inequality
- Large band gaps produce small currents
	- Harder to overcome
	- Less proportion of AM1.5 is high enough energy

Cut-off Wavelength
 $\lambda  \left(\right. 𝜇 m \left.\right) = \frac{1 . 24}{E_{g}  \left(\right. e V \left.\right)}$

![In parallel PV2 v Vlvz V will need to be calculate...](../../../img/OneNote/I-V%20image%207ac63e752f7a3886.png)

![V Fill Factor is the ratio of the Maximum Power V ...](../../../img/OneNote/I-V%20image%20f57ac49572eb2071.png)

- Voc and Jsc
	- Material parameters
- Fill factor
	- Engineering
- Current line not parallel to voltage axis
	- Upwards slope
	- Problem with the shunt
	- Too much recombination
- Voltage line not parallel to current axis
	- Series resistance too high
		- Reduce
	- Increase doping