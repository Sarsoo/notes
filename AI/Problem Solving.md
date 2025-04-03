---
title: 'Problem Solving'
tags:
  - ai
---
# Problem Types
- Toy/game problems
	- Illustrative
- Real world problems
	- Exact solutions

# Intelligent Agents
*Any thing which can be viewed as perceiving its environment through sensors and acting upon that environment through its affectors*

## Reflex
![](img/problem-solving-reflex.png)
## Goal Based
![](img/problem-solving-goal-based.png)
## Utility-based

# Environments
- (in)accessible
- (non)-deterministic
- (non)-episodic
- Static/dynamic
- Discrete/continuous

# Solving
1. Precise problem definition
	- Start conditions and goal state
2. Problem analysis
	- Appropriate representation
	- Problem characteristics
		- Knowledge intensive
		- Decomposability
3. Choice of best technique

# Moves
- Ignorable
	- Simple control structure
- Recoverable
	- Backtrack using control stack
- Irrecoverable
	- Much effort needed for each decision/move

![](img/problem-solving-arch.png)
- Control
	- Cause movement
	- Be systematic
	- Be guided by heuristics

# Predictability
## 8 Puzzle
- Can plan ahead with certainty — only need a   
control structure with backtracking   
	- recoverable, certain outcome  
## Chess
- Future moves are not predictable with certainty.   
- May need to consider several possibilities, and decide best option based on Incomplete information   
- irrecoverable — once a piece is taken cannot in general recover from this state.
- deciding on an optimal move can be difficult
- try to predict opponent's move