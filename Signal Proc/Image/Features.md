---
onenote-id: 0-962c18fa97d20cb91e95ea9ccf99d339!1-D084F068F621FF9!3708
---
- Ideally affine invariant
- Stable over scale
- Repeatable from different views
 
- Corners work

Harris Corner Detector
 
Compare window with one slightly translated

- Autocorrelation of the image
- Sum of square difference
 $\sum_{W} \left[I \left(x_{i} ,   y_{i}\right) - I \left(x_{i} + \Delta x , y_{i} + \Delta y\right)\right]^{2}$  
$\sum_{W} \begin{bmatrix} \begin{bmatrix} I_{x} \left(x_{i} ,   y_{i}\right) & I_{y} \left(x_{i} ,   y_{i}\right)   \end{bmatrix} \begin{bmatrix} \Delta x \\ \Delta y \end{bmatrix} \end{bmatrix}^{2}$ $\begin{bmatrix} \Delta x & \Delta y \end{bmatrix} \begin{bmatrix} \sum_{W} \left(I_{x} \left(x_{i} ,   y_{i}\right)\right)^{2} & \sum_{W} \left(\left[I_{x} \left(x_{i} ,   y_{i}\right) I_{y} \left(x_{i} ,   y_{i}\right)  \right]\right) \\ \sum_{W} \left(\left[I_{x} \left(x_{i} ,   y_{i}\right) I_{y} \left(x_{i} ,   y_{i}\right)  \right]\right) & \sum_{W} \left(I_{y} \left(x_{i} ,   y_{i}\right)\right)^{2} \end{bmatrix} \begin{bmatrix} \Delta x \\ \Delta y \end{bmatrix}$

￼ $\begin{bmatrix} \Delta x & \Delta y \end{bmatrix} C \left(x , y\right) \begin{bmatrix} \Delta x \\ \Delta y \end{bmatrix}$

- C = structure tensor
 
# Eigenvalues

- From C we can get $\lambda_{1}$ and $\lambda_{2}$
- Need high value in both dimensions
	- $\lambda_{1} \lambda_{2} \gg   \lambda_{1} + \lambda_{2}$
	- $D e t \left(M\right) \gg T r a c e \left(M\right)$
- Corner strength = $D e t \left(M\right) - k \cdot T r a c e \left(M\right)$
	- Harris recommends  
        
	- Local maxima highlight corners
- Form window around corner
	- Compute other feature

$\lambda_{1} \lambda_{2} \gg   \lambda_{1} + \lambda_{2}$ $D e t \left(M\right) \gg T r a c e \left(M\right)$

![Machine generated alternative text Detect points o...](../../../img/OneNote/Features%20image%20720f7f8e326be6f5.png)

Bag of Visual Words
 
- Unsupervised clustering
	- Identify mutually distinguishing features
	- Decide number of categories
		- With this given - _semi-supervised_
- Identify interest points
- Plot all features from all images
- Cluster features
- Plot histogram per image for number of interest points in each cluster
- Stop words
	- Remove most frequently occurring codewords
		- Top 5%
		- Common elements that aren't relevant
		- Not discriminative
		- Rarer codewords are more discriminative

k-Means Clustering
  - Separate data into clusters
- Pick k cluster centres randomly in space
- Assign points to neared cluster centres
- Compute mean of each cluster
	1. Move cluster centre to mean

SIFT  
Scale Invariant Feature Transform
 
- Affine invariant
- Defacto standard
- Detecting interest points
	- Key points
- Describing them
	- Descriptor
- Set of _Difference of Gaussian_ images
	- Emphasise image artifact of particular size
	- Points of local max/min
	- Deduce dominant orientation
		- Compute eigenvector of the window
	- Rotate patch according to that angle
- Similar to edge orientation histogram
	- 16x16 grid
	- HOG with n=4, w=4, q=8
		- Window scaled proportional to sigma
- Divide 16x16 into 4x4 grid
- Compute orientation histogram in each cell
- Concatenate histograms to form descriptor
- 16 cells x 8 orientations = 128 dimensional descriptor

![Exported image](../../../img/OneNote/Scale-Space%20image%20ffe5300dbec03e9f.png) ![angle histogram Image gradients](../../../img/OneNote/Features%20image%20b89db73a5bdf622b.png) ![Image gradients Keypoint descriptor](../../../img/OneNote/Features%20image%20e15683f4efaa3e5c.png) ![Exported image](../../../img/OneNote/Features%20image%2099a6a8760f9cde95.png) ![Exported image](../../../img/OneNote/Features%20image%20f96a725a68d2b175.png)

Matching Descriptors
 
- Pair off descriptors, closest first
- Any points that aren't closest other way as well
	- Discard
- Check second closest match
	- 2nd closest distance \< 1.4 x closest distance
	- Discard

![Exported image](../../../img/OneNote/Features%20image%20b536ec279d1777b0.png)

Object Recognition
 
- Build eigenmodel for each category
- Compute Mahalanobis distance between test and each model
- Min distance = class
- Ratio of distances = confidence

Compact  
Discriminative

HOG  
Histogram of Oriented Gradients
 
- Histogram of detected edge directions
- Don't use Sobel
	- Smooths as well
	- 1s throughout
- Threshold for strong edges
	- Variable number of pixels per window
	- Normalise
- Sometimes centre Gaussian to weight histograms
	- Down-weight
- Params
	- W
		- Grid size in cells
	- N
		- Cell size in pixels
	- Q
		- Histogram quantisation per cell
 ![Exported image](../../../img/OneNote/Features%20image%20147c0a49c7da2e87.png)  
![The central cell is centered on the ke oint](../../../img/OneNote/Features%20image%206fcbe0c77d2f9406.png)  

# Pedestrian Detection

- Slide HOG window over detection window
	- Overlap by half a window length
- Get detection window descriptor from aggregated individual descriptors
 ![Detection Window Entire Image](../../../img/OneNote/Features%20image%203a25d1a4d536fa6b.png)

VLAD  
Vector of Locally Aggregated Descriptors
 
- Instead of k-means with hard assignment
- Take into account placement in cluster
 
1. Initialise cluster residual vectors
2. Identify closest cluster
3. Subtract key point from cluster centroid
4. Add relative vector to residual
5. Concatenate residuals of all clusters and normalise
 ![Keypoint desc re Z Cluste centroi 2 3 4](../../../img/OneNote/Features%20image%209b1eaaf908175e90.png)  

- VLAD descriptor is k x d vector
	- K = cluster count
	- D = dimension of feature space

![Term Frequency TF the probability of a codeword te...](../../../img/OneNote/Features%20image%2034efc37fa082ac81.png)
 
VQ  
Vector Quantisation
 
- Coarse representation
- For k-means
	- Simply a count of codewords
	- Information on feature's position within cluster