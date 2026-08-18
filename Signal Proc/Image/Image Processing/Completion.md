---
onenote-id: 0-e001cb364ed40cd917cbb4298be0426c!1-D084F068F621FF9!3708
---
_The (plausible) hallucination of missing detail in photographs_

Applications
 
- Restoration
- Object Removal

Process
 ![Region to fill Image](../../../../img/OneNote/Completion%20image%206110b6902d20396e.png)  

- Given
	- 2D finite domain  
        
	- Smaller domain D
- Required
	- Estimate information in D
		- Based on information in  
            
- Constraints
	- Overall information in domain  
		satisfies some "reasonable criteria"
		- Aesthetically pleasing/semantically plausible
		- Smooth continuation of information across holes

![Exported image](../../../../img/OneNote/Completion%20image%20303d2f2299259d5a.png) ![Exported image](../../../../img/OneNote/Completion%20image%20646d20b03d316d81.png)

_Not necessarily based on semantics_

Laplacian In-Painting  
Interpolation
 $\nabla^{2} f = \frac{𝜕^{2} f}{𝜕 x^{2}} + \frac{𝜕^{2} f}{𝜕 y^{2}}$  
$\begin{bmatrix} 0 & - 1 & 0 \\ - 1 & x & - 1 \\ 0 & - 1 & 0 \end{bmatrix}$  

- See [processing](Image%20Processing.md)
- Smoothest possible interpolation
	- Should be zero when computer over the values proposed for the unknown pixels
 $\underset{f}{m i n} ⁡ \underset{\Omega}{\iint} \left‖\nabla f\right‖^{2}$

- Seek image that satisfies above across $f \left(\right. x , y \left.\right)$ in omega domain
- _Membrane interpolant_
 $\underset{f}{a r g m i n} ⁡ \underset{\Omega}{\iint} \left|\nabla f\right|^{2}     s . t .       \left(f\right|_{𝜕 \Omega} = \left(f^{*}\right|_{𝜕 \Omega}$

- Dirichlet boundary conditions
	- Unknown regions are surrounded by known region
	- Boundaries between are equal
	- ![Known Unknown at boundaries](../../../../img/OneNote/Completion%20image%20e62ce1cef5d946de.png)
- Solve as a linear system
- Don’t need all _known_ pixel to solve
	- Only ones at boundary
 
![Create a design matrix A that is n x n where n is ...](../../../../img/OneNote/Completion%20image%20ed67b7746b473715.png)

- Identity map known pixels
	- Entry in the identity diagonal to map known k to output p
 ![For unknown pixels, encode Laplacian in A local to...](../../../../img/OneNote/Completion%20image%2047d6458e013f2690.png)

- For unknown pixels
	- Set $k   =   0$
		- Desired Laplacian condition
	- Encode Laplacian kernel into row of  
		- Locations that are relative to target  
            
		- Value 4 at column 89

![Exported image](../../../../img/OneNote/Completion%20image%206aa44553754ddcf0.png)

_Harder when the hidden pattern is more complex_

Patch-Based In-Painting  
Texture Synthesis
 
- Instead of interpolating
	- Copy and paste patches
 ![Machine generated alternative text Patch pasted to...](../../../../img/OneNote/Completion%20image%20df547761755db362.png)  

- Present patch as a vector in a feature space
	- Concatenate pixel values
	- Visual search for nearest patch to query patch at destination
		- Euclidean distance
	- Only patch over pixels in the hole
 ![Exported image](../../../../img/OneNote/Completion%20image%20790f99155636bcbb.png)  

- Trade-off between structure representation and coherence
	- Larger patch
		- Complex structure
		- Artifacts
	- Smaller patches better
		- More required

![Orig 20104 patches 11x11 2911 236 patches](../../../../img/OneNote/Completion%20image%200e7b426eb6692d0c.png) ![Orig 51x51 749 patches 21x21 5643 patches 15151 36...](../../../../img/OneNote/Completion%20image%20a6426f3cdfa64c6b.png) ![Original Laplacian Patch based 21x21](../../../../img/OneNote/Completion%20image%207f6bf7a89c8dcf02.png)

Comparison
 
# Interpolation

- Laplacian
- Good for small holes
	- Where background texture is largely absent
- No artifacts
 
# Texture Synthesis

- Patch-based/Freeman-Eros
- Good for large holes
- Structure-aware but edge artifacts