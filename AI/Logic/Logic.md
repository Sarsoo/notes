---
onenote-id: 0-20f61ea995fa05440aed84560afe4424!1-D084F068F621FF9!3714
---
Predicate Logic
 
_A function that maps_ _object arguments_ _as_ _true or false_
 
- E.g. farm_animals(pigs, cattle, sheep)
- Predicate statements are asserted and assumed true as written

![T N.B. functionally complete sets of connectives](../../../../img/OneNote/Logic%20image%207b33f7e3c4fc38da.png)

If … Then ..  
=\>  
Implication  
NOT commutative

![, commutative Distributive Associative AvBvC 0bey ...](../../../../img/OneNote/Logic%20image%201bd39098b6e6edaa.png)

Combining
 
# Conjunction

- Using AND
- Components are conjuncts

# Disjunction

- Using OR
- Components are disjuncts

Logic Order  
Predicate Calculus
 
# 0th

- No variables
- Boolean algebra
	- Commutativity
	- Associativity
	- De Morgan's
 
# 1st

- Variables representing objects
- Universal Quantifier
	- $\forall$
	- For all
- Existential Quantifier
	- $\exists$
	- There exists one or more

$\forall$ $\exists$  
![Vx Feathersx Birdx Birdx quantifiers scope](../../../../img/OneNote/Logic%20image%20eab65f80e91c2c36.png)  

# 2nd

- Variables represent objects or predicates

Vocab
 
- Domain's objects are terms
- Variables ranging over a domain's objects are terms
- Functions are terms
	- Arguments to functions and values returned are objects
- Terms are the only things that appear as arguments to predicates
- Atomic formulas are individual predicates
- Literals are atomic formulas or their negation
- Well-Formed-Formulas (WFFs) are defined recursively
	- Literals are WFFs
	- WFFs connected by AND, OR, NOT, IMPLIES are WFFs
	- WFFs surrounded by quantifiers are WFFs
- A WFF in which all variables are inside the scope of the corresponding quantifier is a sentence
	- ![Vx Feathersx Birdx bound variable](../../../../img/OneNote/Logic%20image%20e10e8b1da855a95e.png)
		- Including y would make it not a proper sentence

![Logic World symbols Predicates OnB,A Function A On...](../../../../img/OneNote/Logic%20image%20c21a872fbfae2d26.png) ![An interpretation is a full accounting of the corr...](../../../../img/OneNote/Logic%20image%20326569266dcc3ad9.png)

Modus Ponens
 ![10 Mel suauod snpow suqsnpuoo sasltuad sunxe b b d](../../../../img/OneNote/Logic%20image%20844ea50b31700410.png)

- If P, then Q
	- P
	- Therefore, Q
- Special case for resolution
 ![is equivalent to](../../../../img/OneNote/Logic%20image%20d3a407c986c179ca.png)  

Modus Tollens
 ![RESOLUTION THEOREM PROOVING 2 resolving clauses re...](../../../../img/OneNote/Logic%20image%208439d2baeb29aa4f.png)  

- If P, then Q
	- Not Q
	- Therefore, not P
- Being an axe murder implies I know how to use an axe
	- I don't know how to use an axe therefore I am not an axe murderer

Resolution & Theorem Proving
 
# Proof By Refutation

- Assume negation of theorem is True
	- Deliberately negate and assume true
- Add to axioms
- Show this leads to a contradiction
	- Conclude that assumed negation of theorem cannot be true
	- Thus the theorem must be true as the negation is false
 ![SIMPLE EXAMPLE we want to prove q given that so co...](../../../../img/OneNote/Logic%20image%20080107259d32a6f7.png)  

# To Clause Form

1. Eliminate implications
	1. ![Exported image](../../../../img/OneNote/Logic%20image%2096dbab7a00f5aab9.png)
2. Move negations to atomic formulas
	1. ![Machine generated alternative text de Morgans theo...](../../../../img/OneNote/Logic%20image%20d2f0b514b4734ad6.png)
3. Rename vars so that quantifiers aren't named the same
4. Purge existential quantifiers
	1. ![Machine generated alternative text i.e. Replace by...](../../../../img/OneNote/Logic%20image%206e1d4274c72d77ec.png)
5. Move all universal quantifiers to far left
6. Move disjuncts down to literals
	1. ![Machine generated alternative text Distributive la...](../../../../img/OneNote/Logic%20image%20192ec5902888e426.png)
7. Eliminate conjunctions
	1. Treat as separate axioms
8. Rename variables

# Example
 ![Machine generated alternative text POO Remove impl...](../../../../img/OneNote/Logic%20image%20038ef188843f3482.png) ![Machine generated alternative text Move universal ...](../../../../img/OneNote/Logic%20image%20807fb564ba185770.png)
 
[Logi2c Symbols](https://en.wikipedia.org/wiki/List_of_logic_symbols)

![Hypothetical syllogism](../../../../img/OneNote/Logic%20image%20fdb023e0b0147a19.png)

Resolution
 
- Produces new clause implied by two clauses
	- Containing complementary literals
- Produces resolvent
 ![al V V V C, where all ai, bi, and c are literals, ...](../../../../img/OneNote/Logic%20image%209ebfa3c02e9685b7.png)

$p \Rightarrow q  \equiv \neg p  \vee  q$  

- Sound rule of inference

1965 Robinson

Computation
 
- Defines how a computer decides which clauses to resolve
- Breadth-first
	- Exhaustive
	- Dumb
	- Goal-seeking agent
	- All possible combinations of clauses
		- Every possible combination of results
- Set-of-Support
	- Pairs selected containing negated theorem or derivatives
	- Steers towards contradictions
- Unit-preference
	- Preference to smallest number of literals
	- Will eventually resolve by eliminating all terms
		- Will eventually combine term and it’s negation
	- Start small
 
# Halting Problem

- Above are complete strategies
	- Will find answer eventually if one exists given enough time