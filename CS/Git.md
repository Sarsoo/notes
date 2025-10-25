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

# Submodules
- `git submodule init`
- `git submodule update`
	- run frequently-ish
- `git clone --recurse-submodules <URL>`
	- on superproject clone
- `git submodule update --init`
	- both, if you didn't clone with `recurse`
- **`git submodule update --init --recursive`**
	- the lot
- `git config -f .gitmodules submodule.<MODULE>.branch <BRANCH>`
	- change tracker of module
- `git submodule foreach 'git <CMD>'`
## updating submodule
1. `cd` into module
2. `git fetch/pull` etc
3. `cd ..`
4. `git commit`
- all in one
	- **`git submodule update --remote [<PATH>]`**
