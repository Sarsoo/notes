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
- Can operate in non-stationary environments
	- Can change weights in real-time
	- In general, more adaptive = more robust
		- Not always though
		- Short time-constant system may be thrown by short-time spurious disturbances
		- Stability-plasticity dilemma

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