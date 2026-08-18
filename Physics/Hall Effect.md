---
onenote-id: 0-11cae87ecf0f059f0418f9f6d7cd2d33!1-D084F068F621FF9!3720
---
![Exported image](../img/OneNote/Hall%20Effect%20image%200039dad528f71dc8.png) ![Trigw Permanent Hall effect wheel speed sensor net...](../img/OneNote/Hall%20Effect%20image%20c26f1aa1a915b875.png)

Lorentz Force
 $F = q \left(E + v \times B\right)$  

- $F$ is force
- $E$ is electric field
- $B$ is magnetic field
- $q$ is electric charge of particle
- $v$ is instantaneous drift velocity

![FqvxB](../img/OneNote/Hall%20Effect%20image%2047583509d325efeb.png)

![Exported image](../img/OneNote/Hall%20Effect%20image%2000aa7b21a6de943a.png)

- Circle coming out of screen
	- Cross into screen

Positive Charge Carriers
 ![Exported image](../img/OneNote/Hall%20Effect%20image%206d7aaed7dae510e8.png)  

- Pass current density in +x
	- Same drift velocity direction as current density
- Magnetic field in Z
 
# Lorentz Force Magnetic Component

$F_{M} = + e \begin{vmatrix} x & y & z \\ v & 0 & 0 \\ 0 & 0 & B \end{vmatrix} = + e \left[\left(0 B - 0\right)   \underset{̲}{x} - \left(v B - 0\right) \underset{̲}{y} + \left(v 0 - 0\right) z\right] = - e v B \underset{̲}{y}$  

- Positive charge carriers deflect to -y
- Magnetic force cannot stay unopposed
	- Current would decay as carriers are forced to one side
		- Hall electric field forms in +y direction
		- FE pointing in +y with magnitude eEy
 $e E_{y} = e v B$  

# Hall Coefficient

$R_{H} = \frac{E_{y}}{j_{x} B_{z}}$  

For positive charge carriers $j_{x} = n e v_{x}$ this is,
 $R_{H} = \frac{E_{y}}{j_{x} B_{z}} = \frac{v B}{n e v B} = \frac{+ 1}{n e}$  

- Good for calculating carrier concentration
 ![F magnetic positive charge Magnetic field carriers...](../img/OneNote/Hall%20Effect%20image%203496bde1a3e8b211.png)

Negative Charge Carriers
 ![Exported image](../img/OneNote/Hall%20Effect%20image%205ec2dc182e480e32.png)

- Lorentz force causes electrons to accumulate at one side
 
# Lorentz Force Magnetic Component

$F_{M} = - e \begin{vmatrix} x & y & z \\ - v & 0 & 0 \\ 0 & 0 & B \end{vmatrix} = - e \left[\left(0 B - 0\right)   \underset{̲}{x} - \left(- v B - 0\right) \underset{̲}{y} + \left(- v 0 - 0\right) z\right] = - e v B \underset{̲}{y}$   
- Same direction as holes
- Magnetic force cannot stay unopposed
	- Current would decay as carriers are forced to one side
		- Hall electric field forms in -y direction
		- FE pointing in -y with magnitude eEy
 
- For negative charge carriers $j_{x} = - n e v_{x}$ this is
 $R_{H} = \frac{E_{y}}{j_{x} B_{z}} = \frac{v B}{- n e v B} = \frac{- 1}{n e}$  
![Magnetic Fm magnetic field B force on negative cha...](../img/OneNote/Hall%20Effect%20image%202b8da740f2e2f7e5.png)

Consequences
 
- Positive coefficient for positive charge carriers and vice versa
	- Measurements on metals indicated that electrons do current carrying
- Confirmed that semiconductors can charge can be carried by either
- When both present, respective mobilities are important
 $R_{H} = \frac{- n 𝜇_{e}^{2} + p 𝜇_{h}^{2}}{e \left(n 𝜇_{e} + p 𝜇_{h}\right)^{2}}$  

![Exported image](../img/OneNote/Hall%20Effect%20image%20463cd5af45beb293.png)  

- V1 and 2 for longitudinal potential difference
- V2 and 3 for transverse Hall potential difference
- Instead of  
	, use  
	- For semantic sake, are applying a current and measuring voltage so makes sense to use resistivity
 $E_{x} = 𝜌_{x x} j_{x}$  

- Tensor for resistivity from  
	to  
    
 
# Longitudinal

$𝜌_{x x} = \frac{E_{x}}{j_{x}} = \frac{\left(V_{x}\right)/L}{\left(I_{x}\right)/W} = \frac{W}{L} \frac{V_{x}}{I_{x}}$  

# Transverse

$𝜌_{y x} = \frac{V_{y}}{I_{x}} = \frac{E_{y} W}{j_{x} W} = \frac{E_{y}}{j_{x}} = \frac{v B}{n q v} = \frac{B}{n q}$  
![Classical pyx Pxx magnetic field B](../img/OneNote/Hall%20Effect%20image%209bba9a472de7f035.png)  
$𝜌_{y x} = \frac{B}{n q}$  
$n = \frac{1}{q} \left(\frac{d 𝜌_{y x}}{d B}\right)^{- 1} = \frac{1}{q} \left(\frac{d V_{y}}{I_{x} d B}\right)^{- 1}$  

$𝜌_{x x} = \frac{1}{n q 𝜇} = \frac{W}{L} \frac{V_{x}}{I_{x}}$ then $𝜇 = \frac{1}{n q 𝜌_{x x}} = \frac{I_{x}}{q} \frac{1}{n v_{x} W/L}$
 $n = \frac{I_{x}}{q} \left(\frac{d V_{y}}{d B}\right)^{- 1}$  
$𝜇 = \frac{1}{n q 𝜌_{x x}} = \frac{I_{x}}{q} \frac{1}{n v_{x} W/L}$  

- Carrier concentration from Hall field
	- Mobility from there