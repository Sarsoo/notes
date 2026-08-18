---
onenote-id: 0-815501a2ef090db116d19abcdec63e3a!1-D084F068F621FF9!3708
---
RGB
 
- Additive
- Similar to our own perception of colour
	- 3 cones
 ![Exported image](../../../img/OneNote/Colour%20image%20ca56c0d4946d169c.png)  
![Exported image](../../../img/OneNote/Colour%20image%20ad9bcea83df1f503.png)  

![Exported image](../../../img/OneNote/Colour%20image%20250d90652316646f.png)

Perceived Luminosity
 $l \left(r , g , b\right) = 0 . 30 r + 0 . 59 g + 0 . 11 b$

CLUT  
Colour Lookup Table
 
- Old way to map to limited colours
- 1 byte per pixel
	- 8-bit
 ![Exported image](../../../img/OneNote/Colour%20image%201d46744f6aefb6ef.png)  

# True Colour Framebuffer

- 3 bytes per pixel
	- 24-bit

![Exported image](../../../img/OneNote/Colour%20image%202fc13f8712cb2b20.png)  

CRT
 ![Exported image](../../../img/OneNote/Colour%20image%204b426280bdd22cbd.png)  
$I = P^{𝛾}$

- $I = P^{𝛾}$
	- Gamma typically around 2.2 for a typical CRT
	- Lower pixel intensities (power) produce less physical response on CRT
		- Appears darker than it should
		- Correct gamma
 
# Gamma Correction

- Correct output by factor of 1/2.2=0.45
- Still done due to international standardisation

![Exported image](../../../img/OneNote/Colour%20image%2031b4a1a856287483.png)  

Capturing Images
 
# CCD

- Buckets
- Regular intervals, charge in buckets is measured and cleared
- SNR often poor in low light

![Exported image](../../../img/OneNote/Colour%20image%20fa9eb14d15c83971.png)

# CMOS

- Each photosensor hardwired directly
	- More precise sensing

![Exported image](../../../img/OneNote/Colour%20image%2078aea8afadf5c12e.png)  

# Bayer Pattern

- Only one sensor per pixel
	- Need colour
- Demosaicing algorithm
	- Interpolate missing RGB data

![Exported image](../../../img/OneNote/Colour%20image%203bf6d163dfe9387d.png)  

CMY
 
- Subtractive
- Green ink absorbs magenta
	- Reflected yellow + cyan = green
 ![Exported image](../../../img/OneNote/Colour%20image%202e0059e84278c97b.png)  
![Exported image](../../../img/OneNote/Colour%20image%20fd319333c37de7a9.png)  
![Exported image](../../../img/OneNote/Colour%20image%2049cd9840f086c5dc.png)  

# RGB-CMYK

- K is black

|   |   |
|---|---|
|![Exported image](../../../img/OneNote/Colour%20image%20a3915d84a16b9da5.png)|![Exported image](../../../img/OneNote/Colour%20image%209c687e72235d2785.png)|
 ![Exported image](../../../img/OneNote/Colour%20image%200dfa7f2faee87e15.png)  

Tri-Stimulus
 
- **Can additive RGB encode any colour we want?**
	- **No**
- User observes target colour patch under white light
- Adjusts RGB lights shining on white patch to match colour
 ![Exported image](../../../img/OneNote/Colour%20image%200214825984678f93.png)  

- Red cone overlaps with Blue in lower end
	- Not independent
 ![Exported image](../../../img/OneNote/Colour%20image%20a60e87e61882993c.png)  

- Difference limen non-linear
 ![Exported image](../../../img/OneNote/Colour%20image%20ad145d6f046c52dd.png)  

CIE  
Commission Internationale de L’Eclairage
 
- Additive model
- X, Y, Z instead of R, G, B
	- CIEXYZ
- Ideal primaries
	- Not physically realisable
 ![Exported image](../../../img/OneNote/Colour%20image%2058730fd4c871e7e4.png)  

# Normalised

![Exported image](../../../img/OneNote/Colour%20image%202189bcc92db265f3.png)

- Typically pick max of X, Y, Z to be non-normalise
	- Represent brightness of colour
	- Luminance

![Exported image](../../../img/OneNote/Colour%20image%204d75d9ab080b4b9d.png)

- Tri-stimulus Space
	- Y
		- Luminance
		- 1 Channel
	- x, z
		- Chromaticity
		- 2 Channels
- Perceptually corrected version
	- CIELab space
 ![Exported image](../../../img/OneNote/Colour%20image%20f22268006469572a.png)

- White point
	- $x = y = \frac{1}{3}$

$x = y = \frac{1}{3}$  
![Exported image](../../../img/OneNote/Colour%20image%20abd07777577ad1dc.png)  

# RGB-CIEXYZ

- RGB is not standard
	- Use sRGB
 ![Exported image](../../../img/OneNote/Colour%20image%208ae89e6a8f781564.png)  

HSV
 
- More intuitive
- Hue
	- Chromaticity/wavelength
- Saturation
	- How washed out
	- How much of that colour
- Value
	- Approximates luminance
- HSL
	- Hue/Sat/Luminance
	- Similar
- Skin tones have similar {H, S} values throughout
 ![Exported image](../../../img/OneNote/Colour%20image%20cac61b34ce22e15a.png)  
![Exported image](../../../img/OneNote/Colour%20image%20755c1c2522aee5e6.png)  
![Exported image](../../../img/OneNote/Colour%20image%202b9bf12a14c9b475.png)  

# RGB-HSV

- Saturation
	- $W = m i n ⁡ \left(\right. R ,   G ,   B \left.\right)$
	- $S = 1 - W$
	- Amount of white is how desaturated it is
- Value
	- $V = m a x ⁡ \left(\right. R ,   G ,   B \left.\right)$
	- HSL can use luminance equation
- Hue
	- Subtract W from RGB colours
	- $R G B \left(0 . 3 ,   0 . 6 ,   0 . 2\right) \Rightarrow \left(\right. 0 . 1 ,   0 . 4 ,   0 . 0 \left.\right)$
		- $W = m i n ⁡ \left(R ,   G ,   B\right) = 0 . 2$
	- Use two non-zero components
		- $\frac{0 . 4}{0 . 4 + 0 . 1} = \frac{4}{5}$
		- 4/5 round the arc from red -\> green
		- H = 4/5 x 120 degrees = 96 degrees
		- For W = B, H = H + 0
		- For W = R, H = H + 120
		- For W = G, H = H + 240

$W = m i n ⁡ \left(\right. R ,   G ,   B \left.\right)$ $S = 1 - W$ $V = m a x ⁡ \left(\right. R ,   G ,   B \left.\right)$ $R G B \left(0 . 3 ,   0 . 6 ,   0 . 2\right) \Rightarrow \left(\right. 0 . 1 ,   0 . 4 ,   0 . 0 \left.\right)$ $W = m i n ⁡ \left(R ,   G ,   B\right) = 0 . 2$ $\frac{0 . 4}{0 . 4 + 0 . 1} = \frac{4}{5}$