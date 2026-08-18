---
onenote-id: 0-0207836469644803a97e65c30ee02d55!1-D084F068F621FF9!3928
---
Characteristics
 
- Inexpensive motes
	- Low bandwidth
- Large numbers of nodes
- Coordination
- Information reported for processing
	- Or communicated to other device
- Typically application-dependent

Non-Standard Sensors
 
- Human-as-sensor
	- Citizen sensor
	- Tweeting
- Software sensors
	- Bots

Big Data
 
- Reliable
- Efficient
	- Low power
- Scalable

Access
 
- Pub/Sub
- Ad-hoc Query
	- Fields
		- ID
		- Location
		- Type
		- Time
	- Types
		- Entity of interest
 
Metadata
 
- Numbers not useful on their own
- Need metadata
	- Measurement unit
	- Location
	- Time
	- Precision/Accuracy

Processing Points
 
# In-Network

- Aggregation
	- Collate and summarise
	- Trends might be enough
	- Min/Max/Average/Sum
- Single or multi-node
- Temporal correlations
	- Values might not change quickly or often
- Spatial correlations
	- Neighbouring nodes might have similar values
	- Can track event using known locations
 
# Back-end

Data-Centric Networking
 
- When redundantly deployed, specific source not important
	- Think more event-based
- Focus network transactions on data itself
 
- Address-centric
	- Internet, IP
- Node-centric

Aggregation
 
- Smaller representation of data
	- Min/max/mean
		- Lose granularity
- Advanced could reduce dimensionality
	- PCA
- Represent patterns/abstractions
	- Compress as you go in multi-hop networks
- Usually closer to source
 ![Exported image](../../../../../img/OneNote/Data%20image%209d513b4c77d4766c.png)  

# Efficacy

- Accuracy
	- Difference between resulting and original representation
	- Lossless or lossy
- Completeness
	- % of data included in final representation
- Latency
	- Computation & report time
- Overhead
	- Trade-off between accuracy, latency and overhead

Statistical Processing
 
- Time-series
- Techniques
	- Clustering
	- Classification
	- Regression
	- Prediction
- Segment length
	- Fixed-time
	- Fixed-sample
	- Expanding window
	- Overlapping windows
- Representation
	- Can reduce dimensionality
	- Often lossy

Symbolic Aggregation Approximation  
SAX
 
- Symbolic string
- Extends Piecewise Aggregate Approximation (PAA)
- Simple & low computation
- Allows use of other methods on strings
	- Hashing
	- Pattern matching
	- Suffix trees
- Arbitrary length
 
1. Transform to PAA
	1. Average over time
2. Convert PAA to string
 
1. Window data
2. Z-normalise
3. PAA
	1. Merging process
	2. Average
4. Assign alphabet to each frame
 ![Exported image](../../../../../img/OneNote/Data%20image%203c4d964f21101d66.png)  

# PAA

- Normalise
	- Interested in fluctuations
	- Not actual values
	- Allows comparisons of different series
- Window into equal-sized frames
	- Mean value per frame
 
# Breakpoints

- Range on normal distribution
- With same probability density area in between
 ![SAX example, step 3 SAX alphabet cuts 10 Time tick...](../../../../../img/OneNote/Data%20image%20080975184a05a288.png)  

# Distance Measures

- Euclidean
	- ![Exported image](../../../../../img/OneNote/Data%20image%206cf6c895183a27dd.png)
- PAA
	- ![Exported image](../../../../../img/OneNote/Data%20image%2090cdd959997767b9.png)
- Piece-wise probability density
	- ![E distQt,](../../../../../img/OneNote/Data%20image%20031686322aa48bf6.png)
      
	- ![0, if Ir cl 1 min r,c, otherwise](../../../../../img/OneNote/Data%20image%204b742859c09db3c8.png)
    
[jmotif - SAX](https://jmotif.github.io/sax-vsm_site/morea/algorithm/SAX.html)  
[jmotif - PAA](https://jmotif.github.io/sax-vsm_site/morea/algorithm/PAA.html)  
[Vignesh Krishnamoorthy - PAA](https://vigne.sh/posts/piecewise-aggregate-approx/)
 
[PyTS - PAA](https://pyts.readthedocs.io/en/stable/modules/approximation.html)
 
[Riverside, Eamonn - SAX](http://www.cs.ucr.edu/~eamonn/SAX.htm)

_“The central limit theorem states that under certain (fairly common) conditions, the sum of many random variables will have an approximately normal distribution”_
 $z_{i} = \frac{\left(c_{i} - 𝜇\right)}{𝜎}$

