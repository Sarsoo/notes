---
title: Git
---
# Selections
- `@{n}`
	- reflog
```bash
$ git reflog
734713b HEAD@{0}: commit: Fix refs handling, add gc auto, update tests
d921970 HEAD@{1}: merge phedders/rdocs: Merge made by the 'recursive' strategy.
1c002dd HEAD@{2}: commit: Add some blame and merge stuff
1c36188 HEAD@{3}: rebase -i (squash): updating HEAD
95df984 HEAD@{4}: commit: # This is a combination of two commits.
1c36188 HEAD@{5}: rebase -i (squash): updating HEAD
7e05da5 HEAD@{6}: rebase -i (pick): updating HEAD
```
- `^`
	- *parent of*
	- `^n`
		- nth parent (merges)
- `~`
	- *first parent of*
	- `HEAD~ == HEAD^`
	- `~~`/`~2`
		- *parent of parent of*
`HEAD~3^2`
- 2nd parent of third ancestor of
# Ranges
- `X..Y`
	- *commits on `Y` that aren't on `X`*
	- `git log X..Y`
	- `X..` == `X..HEAD`
- `^X`
	- *not on*
	- `--not X`
	- `^X Y` = `X..Y`
	- Can use with more than two refs
- `X...Y`
	- *commits on X that aren't on Y and on Y that aren't on X*
	- *symmetric difference*
	- `--left-right`
		- Gives `>` or `<` for which side it's on