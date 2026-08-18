---
onenote-id: 0-e0837cabf51d02331089c47e4a4e5964!1-D084F068F621FF9!3714
---
_Game playing can help us to understand how (intelligent) humans behave by trying to describe human behaviour in a competitive environment._

- Game-specific knowledge
- Methods of search reduction
- Game-specific search methods

Von Neumann & Morgenstern
 ![14 7 3 5 2 4](../../../img/OneNote/Adversarial%20Game%20image%203fd3b196728271d2.png)  
![0M8 10 11 12 13 14 15](../../../img/OneNote/Adversarial%20Game%20image%20b4c9d0fa2acf5534.png)

- Equivalent tree

Strategy
 
How to make the next move given rules, knowledge and some estimators of how to assess the ‘goodness’ of a given possible next move

- Wining
	- A method, repeatedly applied to many moves leading to a win wherever one is possible

# I

Initial State
 
# O

Operators

- Legal moves or operations on pieces
 
# T

Terminal Test

- Ability to check whether the game has ended
 
# U

Utility function

- Numeric value at tend of the game if T is set
	- Game over
- Points for a win, loss, draw
 
# 2 Steps

- Game Tree Generation
- Game Tree Evaluation

Minimax
 
- Generate game tree to a terminal node
- Evaluate all terminal nodes using U
- Select a path back to MAX's move which guarantees a WIN
- Follow path to WIN
 
Designed for MAX to win
 
_The minimax value of a player is the smallest value that the other players can force the player to receive, without knowing the player's actions; equivalently, it is the largest value the player can be sure to get when they know the actions of the other players_
 $\overset{-}{v_{i}} = \underset{a_{- i}}{m i n} ⁡ \underset{a_{i}}{m a x} ⁡ v_{i} \left(a_{i} , a_{- i}\right)$  

- In reality
	- Memory-bounded
	- How to select 'best' path
- Not as good as expert players
	- No pattern recognition
- Computer assumes other player makes optimal move
 ![MlN 32 12 13 8 2 4 6 14 5 2](../../../img/OneNote/Adversarial%20Game%20image%20bf0b8323d383ce41.png)  

- /\ = moves by MAX
- \/ = moves by MIN
- High numbers good for MAX
- Similar to depth-first
- Pick best of three options for actor making decision
	- Min moves A11 up t A1
	- Max picks A1 because it's the highest he can get

Evaluation Functions
 
- Shannon
	- 1950
	- Behaves like depth first
		- Really like depth limited
	- (Static) evaluation function
	- Cut-off test
	- Same function for both players
		- High/low better for either
	- E.g. chess = $\left(v_{w}\right)/\left(v_{b}\right)$
	- E.g. checkers = c

Horizon Effect
 
- Not able to look far enough ahead
 ![Pawn lost horizon Queen lost](../../../img/OneNote/Adversarial%20Game%20image%20289507446d7d3354.png)  

Layer = ply

Heuristic Pruning
 
- Plausible moves searched for greater depth
- If numbers are swinging wildly between players
	- Keep searching for a stable area
	- Quiescence
- If moves look bad
	- Prune off whole sub-tree

Alpha Cut-Off
 
_Occurrence of an a value that is less than or equal to an a value 2 plies higher up the tree allows pruning of all branches originating from the intervening minimising ply_
 ![asn](../../../img/OneNote/Adversarial%20Game%20image%204b4a53bc0a21b0bf.png)  

- 11 is definitely going to be picked by MIN
	- Doesn't matter what the rest of the sibling branches
	- MIN will always pick it
	- Bad branch

Beta Cut-Off
 
_Occurrence of a b value that is greater than or equal to a b value 2 plies higher up the tree allows pruning of all branches originating from the intervening maximising ply_
 ![15 18 MlN MlN](../../../img/OneNote/Adversarial%20Game%20image%20907f6fc43b75c669.png)  

- 18 greater than 15
	- MIN can see it coming and will avoid
	- Skip the rest of the sibling branches

![MlN 32 22 12 13 8 23 14 5 2](../../../img/OneNote/Adversarial%20Game%20image%209b9cf36e068c2a3c.png)

Characteristics
 
- Worst-case scenario
	- No saving
- Best-case scenario
	- Both players best move is left most at each branch