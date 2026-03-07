---
tags:
  - maths/signals
---
# Dynamic vs Algebraic
- Dynamic system has "memory", output depends on present and past
	- Includes diff and/or integral operators with initial conditions
	- Cap and or inducer
- Algebraic
	- No calculus operators
	- Output depends only on input

# Time Invariant vs Time-Varying

# Continuous vs Discrete time

# Linear vs Non-Linear

# Deterministic vs Stochastic
- Deterministic
	- Output fully determined by parameter inputs
- Stochastic
	- Include randomness
		- Noise/Disturbance
	- Same inputs can lead to different outputs

# Lumped vs Distributed parameters
- Lumped
	- Only one independent variable (time $t$)
	- Typical for electrical systems
	- $x(t)$
	- Ordinary differential equations
- Distributed
	- Several independent variables
		- time, pressure, temperature
	- Typical for chemical processes and process control
		-$x(t, P, T)$
	- Differential partial equations

# Causal vs Non-Causal
- Causal
	- Output depends only on current and past values
- Non-Causal
	- Output depends on future inputs

# SISO vs MIMO
- Single Input/Single Output
- Multiple Input/Multiple Output