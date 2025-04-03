---
title: 'Training'
tags:
  - ai
---
# Modes
## Sequential
- Apply changes after each train pattern
- Less local storage for each synaptic connection
- Search in weight space stochastic
	- Patterns presented to network in random order
	- Less likely to fall into local minima
- Difficult to establish theoretical conditions for convergence

## Batch
- Apply changes at the end
- Accurate estimate of gradient vector
- Can guarantee convergence to local minimum