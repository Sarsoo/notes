# Linearity
- Neurons can be linear or non-linear
- Network of non-linear neurons is non-linear
- Non-linearity is distributed
- Helpful if target signals are generated non-linearly

# Input-Output Mapping
- Map input signal to desired response
	- Supervised learning
- Similar to non-parametric statistical inference
	- Non-parametric as in no prior assumptions
	- No probabilistic model

# Adaptivity
- Synaptic weights
	- Can be easily retrained
- Stationary environment
	- Essential statistics can be learned
	- Model can then be frozen
- Non-stationary environments
	- Can change weights in real-time
	- In general, more adaptive = more robust
		- Not always though
		- Short time-constant system may be thrown by short-time spurious disturbances
		- Stability-plasticity dilemma
	- Not equipped to track statistical variations
	- Adaptive system
- Linear adaptive filter
	- Linear combiner
		- Single neuron operating in linear mode
	- Mature applications
	- Nonlinear adaptive filters
		- Less mature
- Environments typically considered pseudo-stationary
	- Speech stationary over short windows
- Retrain network at regular intervals to account for fluctuations
	- E.g. stock market
- Train network on short time window
	- Add new data and pop old
		- Slide window
	- Retrain network

# Evidential Response
- Decisions are made with evidence not just declared
	- Confidence value

# Contextual Information
- Knowledge represented by structure and activation weight
	- Any neuron can be affected by global activity
- Contextual information handled naturally

# Fault Tolerance
- Hardware implementations
- Performance degrades gracefully with adverse conditions
- If some of it breaks, it won't cause the whole thing to break
	- Like a real brain

# VLSI Implementability
- Very large-scale integration
	- Chips with millions of transistors (MOS)
	- E.g. microprocessor, memory chips
- Massively parallel nature
	- Well suited for VLSI

# Uniformity in Analysis
- Are domain agnostic in application
	- Analysis methods are the same
	- Can share theories, learning algorithms

# Neurobiological Analogy
- Design analogous to brain
	- Already a demonstrable fault-tolerant, powerful, fast, parallel processor

- To slight changes
	- Rotation of target in images
	- Doppler shift in radar
- Network needs to be invariant to these transformations

# Invariance
1. Invariance by Structure
	- Synaptic connections created so that transformed input produces same output
	- Set same weight for neurons of some geometric relationship to image
		- Same distance from centre e.g.
	- Number of connections becomes prohibitively large
2. Invariance by Training
	- Train on different views/transformations
		- Take advantage of inherent pattern classification abilities
	- Training for invariance for one object is not necessarily going to train other classes for invariance
	- Extra load on network to do more training
		- Exacerbated with high dimensionality
3. Invariant Feature Space
	- Extract invariant features
		- Use network as classifier
	- Relieves burden on network to achieve invariance
		- Complicated decision boundaries
	- Number of features applied to network reduced
	- Invariance ensured
	- Required prior knowledge