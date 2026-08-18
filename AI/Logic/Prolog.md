---
onenote-id: 0-4157a52c24fe0fc31510f3b0a5323367!1-D084F068F621FF9!3714
---
![Example Proqram parent pam, bob parent tom, bob pa...](../../../../img/OneNote/Prolog%20image%2075fb6ff8ce829955.png)

- Roots in first-order logic
- Declarative
- Relations
	- Rules
	- Facts

Modes
 
- Query
	- Run a query on the rules
- Assertion
	- Add rules and relations

Syntax
 
- Won’t get angry at a misspelling
	- Just says no
- Lowercase
	- Constants
- Uppercase
	- Variables
- Full stop
	- End of query
- Commas
	- Logical AND
- :-
	- Rules

Rules  
:-
 
- Use universal quantification
- $\forall$
- offspring(Y, X) :- parent(X, Y)
	- Prolog clause
	- Fact is a unit clause
	- Conclusion
		- Head of clause
		- LHS
	- Condition
		- Body of clause
		- RHS
	- Conclusion is true if condition true

$\forall$

Recursion
 ![For All X and Z X is a predecessor of Z if X is a ...](../../../../img/OneNote/Prolog%20image%2076b70d9f58a1a8c2.png)  

![sister relation sister X, Y parent Z, X, parent Z,...](../../../../img/OneNote/Prolog%20image%200063f8f6764e5107.png)

Circuits
 ![10 7 orl 4 andl,l,l.](../../../../img/OneNote/Prolog%20image%207ed70741c7de5ff1.png)  
![xorlnl ,ln2,Out ? xorl , 1 ,out. OutO Forward simu...](../../../../img/OneNote/Prolog%20image%20a10c06d22cf7806a.png)

![Variables and terms A logic variable stands for si...](../../../../img/OneNote/Prolog%20image%20b3c04f711efbafed.png)

List
 ![List is a binary structure first argument is an el...](../../../../img/OneNote/Prolog%20image%200f89aa7c3e8e572b.png)  
![append Xs, Ys, XsYs XsYs is the result of concaten...](../../../../img/OneNote/Prolog%20image%20edd3da22a8a2aaef.png)  
![TRUE a,bl, Ys CD Output Xs append Xs1, Ys, b,cl TR...](../../../../img/OneNote/Prolog%20image%20a8e838d801e8897f.png)  

# Reverse

![reverse List, RevList RevList is the result of rev...](../../../../img/OneNote/Prolog%20image%204ec96ea741db2444.png)  
![An extra argument can be used to build bottomup re...](../../../../img/OneNote/Prolog%20image%20392b08418c590e7b.png)

Arithmetic
 ![For efficiency uses builtin operators e.g. X is 3 ...](../../../../img/OneNote/Prolog%20image%2003c929dc45307c5c.png)

Mapping
 ![mapping Xs, Ys Ys is the result of applying a mapp...](../../../../img/OneNote/Prolog%20image%2043421b9090cab13a.png)  

![simple objects variables numbers atoms structures ...](../../../../img/OneNote/Prolog%20image%20b4657bfa65c611af.png)

Cut  
!
 
- Reduce search space by dynamically pruning search tree
- Easier to understand procedurally than declaratively
- Wont backtrack past !
- Green cuts don’t change declarative meaning of program
- Red cuts change meaning
 ![A Bl, .... Bk2, .... if failure occurs in goal Bk2...](../../../../img/OneNote/Prolog%20image%2031733d548d50b7a7.png)  
![member X, X I Ll member X, Y I Ll member X, L. Thi...](../../../../img/OneNote/Prolog%20image%20a6b58ad79da2e98a.png)

- Defines X as member of a list if it is in head or tail
	- Will only get a as answer and no more
		- Search space pruned
 
# Negation as Failure

- Not(G) succeeds if G is in finite failure set
- Search tree is finitely failed if no success nodes or infinite branches
- Closed world assumption
 ![loves john, mary. loves jim, mary. not loves ken, ...](../../../../img/OneNote/Prolog%20image%2097e4a72db27acd71.png)  
![tsess stem redicate fail that alwa s fails not X i...](../../../../img/OneNote/Prolog%20image%207d3f9013fd97c37a.png)

- X ! Fail
	- If X exists it runs through the ! to get to fail
		- Wont back track
	- If it doesn't exist it will short circuit the first one and hit the second

I/O
 
- read(X)
	- Reads term from input stream
- write(X)
	- Writes X to output stream
- assert(C)
	- Add clause C
	- asserta, assertz adds to beginning and end
- retract(C)
	- Deletes first clause matching C
 ![writeln Xs writes a list of terms on current outpu...](../../../../img/OneNote/Prolog%20image%20916c71d6ef00d1d0.png)
 ![Example procedure p Tl, T2....Tn name and arity Ty...](../../../../img/OneNote/Prolog%20image%202a8dbda743752e6e.png)  
![o initial comments can include what the program is...](../../../../img/OneNote/Prolog%20image%207a530467078d5086.png)

- Program
	- List of clauses
		- Facts
		- Rules
		- Questions
- Procedure
	- Clauses related to same relation
 
Backtracking
 ![Exported image](../../../../img/OneNote/Prolog%20image%201bdad5954c0b7843.png)  
![boy tom . boy bob . girlalice girllili pay X,Y . b...](../../../../img/OneNote/Prolog%20image%20a1b4b04c886b2624.png)  
![payX, Y boytom girlalice girl lili boybob girlalic...](../../../../img/OneNote/Prolog%20image%20425dc1733838b42f.png)