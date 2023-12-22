---
tags:
  - ai
---

## Design Parameters
- Size of input image
	- 256 x 256 x 1
	- Towards top end of supportable
- Padding
	- Thickness of border 0s
- Kernel size
	- 7 x 7 x 1 x n
		- N is for multiple filters per layer
	- Main design decision
		- 12 x 12/15 x 15 in early layers
		- Lower in later filters
		- Dataset-dependent
- Stride
	- Interval to sample
	- 1
		- Every subsequent pixel
		- Same size out as in
	- 2
		- Every other subsequent pixel
		- Out image is half input size
- Size of computable output
	- 252 x 252 x 1 x n
		- Depends on padding and striding