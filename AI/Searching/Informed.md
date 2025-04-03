---
title: 'Informed'
tags:
  - ai
---
# Best First

- Uniform cost uses an evaluation function
	- Doesn't necessarily direct towards goal
	- Doesn't know how far to goal
		- Only cost so far
	- Still blind
- Look forward
	- Lot of techniques aiming to define best node

1. Expand node closest to goal
	- Greedy
2. Expand node on least cost solution path
	- A*

# Greedy
- **Estimate** distance to goal
	- Often can't determine exactly
	- This cost is a heuristic
- Could be crow-flies distance
- Expand nodes in increasing order of heuristic cost
- **Fast**
- **Not optimal**
	- Simple heuristic

# A*
- Combines advantages of uniform cost and greedy search
- ***Optimal & Complete***
- $h(n)$
	- Estimate of distance to goal
	- Greedy
- $g(n)$
	- Cost of cumulative path
	- *Uniform cost*
- $f(n)=g(n)+h(n)$
- Heuristic must be ***admissible***
	- Underestimates the distance to the goal
	- Never overestimates
	- Monotonic
- Expand other low cost paths
- Pathmax
	- For heuristics which might not be monotonic
	- Select last option if going in wrong direction