---
onenote-id: 0-40ed0bcf5be6064f3b4b0740e26a7969!1-D084F068F621FF9!3708
---
Snakes are piecewise curves that are iteratively fitted to image data by moving their control points (snake is like an “elastic band”)

- Top-down
- Search space of possible solutions
	- Solution is configuration of control points

Optimisation
 ![Machine generated alternative text dP2s dPs ds dS2...](../../../img/OneNote/Active%20Contours%20image%2078ac1be09280930b.png)  

- Minimise energy,  
    
- Alpha
	- Regularises control point spacing
- Beta
	- Controls curvature
- External
	- Based on image content $I \left(\right. . \left.\right)$
		- At $P \left(s\right)$
 
# Weird Weights

- Low weight on  
	- Spacing between points irregular
	- Leads to loss of accuracy
- Low weight on  
	- Curvature can be high
	- Sharp discontinuities in curves
		- Doubling back
- Low weight on  
	- Snake doesn't fit underlying data well
 ![Exported image](../../../img/OneNote/Active%20Contours%20image%204966fda7eec37779.png)  

![Machine generated alternative text 2ND Solution sp...](../../../img/OneNote/Active%20Contours%20image%20f182e2d0c6c396ee.png)  

- Space is smooth
	- Good solutions near other good solutions

Gradient Descent
 ![Machine generated alternative text E for ps Bad so...](../../../img/OneNote/Active%20Contours%20image%20ce06f9c6cefa478d.png)  
$E \left(x + \delta , y\right) = \frac{\delta E \left(x , y\right)}{\delta x}$  
$E \left(x , y + \delta\right) = \frac{\delta E \left(x , y\right)}{\delta y}$  

Move in direction of $- v e$
 
- Space is high dimensional
	- High dimension vector of energy
 ![Machine generated alternative text GRADIENT X2 EXl...](../../../img/OneNote/Active%20Contours%20image%20f156871642abd3dc.png)

Williams Shah Fitting
 
- Alternative greedy approach
- Limits discontinuities early in fitting
	- Allows near convergence
 
1. For each control point, in turn, move the control point to the location in its 3x3 neighbourhood minimising E.
2. If the follow criteria are met, set b to zero at the control point:
	1. curvature at control point larger than both its neighbours
	2. curvature at control point is larger than a basic threshold
	3. the control point is over a strong edge pixel

Point Distribution Model
 
- Build statistical shape model from set of contours
- Eigenmodel
 ![Machine generated alternative text X3,Y3 X2,Y2 XI,...](../../../img/OneNote/Active%20Contours%20image%2052438b18428829c1.png)  
![Machine generated alternative text 2nD space Each ...](../../../img/OneNote/Active%20Contours%20image%20e367a4c91b2a984f.png)  

- Major issue is creating correspondence between points

Procrustes
 
- Align edge maps by
	- Translating
	- Rotating
	- Uniformly Scaling
 
1. Translate centroid to align models
2. Rotate model to minimise the Sum of Squared Differences
3. Scale model to minimise SSD
 ![Exported image](../../../img/OneNote/Active%20Contours%20image%20fe5afb33776a8ba3.png)

Active Shape Model
 
- Perform gradient descent in Eigenmodel space
	- Instead of raw 2N+D space
 ![Machine generated alternative text 1 Vary points b...](../../../img/OneNote/Active%20Contours%20image%206ac22f5017c44a0e.png)