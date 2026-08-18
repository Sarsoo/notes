---
onenote-id: 0-e418d81b6c5501761defe455d76ff80a!1-D084F068F621FF9!3714
---
![Leastsquares LS estimation based on minimum mean s...](../../../../img/OneNote/Training%20image%201bc2889f3735284f.png)

Uses prior information

Maximum Likelihood
 
- To find  
	- General
		- a, b matrix
 ![Machine generated alternative text O POtrainI Dc](../../../../img/OneNote/Training%20image%2068bf92069c3d5d3f.png)

- Set derivative to zero
	- Find maxima
- Use logs because monotonic
 
- Viterbi simpler
	- Hard decisions
- Baum-welch more sophisticated
	- Soft allocations

Viterbi
 
- Use optimal path from Viterbi algorithm
 ![POlA](../../../../img/OneNote/Training%20image%20190ce1165d5bf644.png)

- Approximate using best path
- Binary decision
	- _Are we in the best state right now or not_
	- $q_{t} \left(i\right) \in \{ 0 , 1 \}$

$q_{t} \left(i\right) \in \{0 , 1\}$  
![Statetransition probabilities, Etl qti 1 where sta...](../../../../img/OneNote/Training%20image%202df464de30ff6e62.png)

- Was on the best at $t - 1$ and again at $t$ ( $i$ and $j$ on numerator)
- How many times did we jump to state  
	from  
	- Normalised by how many times we were in  
		at all
 ![Discrete output probabilities, bjk Etl 1 where eve...](../../../../img/OneNote/Training%20image%209b630e8344fd7168.png)

- Omega
	- Indicator function for observations
	- $k$ is class
		- e.g. Red
 
# Multiple Sequences
 
For  
of  
sequences

![a b Statetransition probabilities, Efl Erl Etl Dis...](../../../../img/OneNote/Training%20image%20a726f2937a734537.png)

Baum-Welch  
Expectation Maximisation
 
- Soft assignment
	- Occupation likelihood
	- Instead of indicator functions
 ![Exported image](../../../../img/OneNote/Training%20image%204d38306e07c66407.png)  
![PO,xt iti p 0 p 0](../../../../img/OneNote/Training%20image%2095766b43544ce6f8.png)  
![ati 3i](../../../../img/OneNote/Training%20image%204d5b5bebffa6196c.png)

- Bayes
- Alpha, beta and P of observations given model computed using forward or backward procedure
- Numerator
	- Turns into likelihoods
	- Forward
		- Joint probability of observations up to  
			and being in state  
			at time  
            
	- Backward
		- Probability of observations after current time given that in state  
			at time  
            
	- Combine to give both
 
# Transition Likelihood
 
- Weight for particular transition through trellis

![i, xt jlO, Pxtl P ot,xt jlxtl X P 01 ,Xt1 POI Ot 1...](../../../../img/OneNote/Training%20image%20e5db65ad11c44d64.png)  
![Exported image](../../../../img/OneNote/Training%20image%20e436b78ef8e7008f.png)  

# Re-estimate Parameters
 ![Statetransition probabilities, aij Etl](../../../../img/OneNote/Training%20image%20c02418e7955c19f3.png)

- Transition likelihoods
	- At point in trellis
	- Times we went from  
		to  
        
	- Normalise by times we were in state  
        
	- Essentially same meaning as Viterbi
 ![Discrete output probabilities, Etl](../../../../img/OneNote/Training%20image%203bc3afaa6cb61b97.png)

- $q$ from Viterbi has become soft weights (occupation)
 
- Use new parameters to create new model

![P O trainl P O trainl](../../../../img/OneNote/Training%20image%20c369e85e76fa2183.png)

- Guaranteed to be greater or equal

State transition & emission

![Initial HMM Forw arcLB ack Ward A Igorithm Update ...](../../../../img/OneNote/Training%20image%20dbdfcc4b4ea674ef.png)

Flat Start
 
- Set models equal to global statistics for data
- Same each time
	- Can't tell whether at global or local maxima
 
Random
 
- Perturbations encourage finding global maxima

![Machine generated alternative text Estep Forward l...](../../../../img/OneNote/Training%20image%20fdda811c97148149.png)

- E
	- Associations between observations from training data and model parameters
	- Mainly in terms of model states
	- Occupation and transition likelihoods
- M
	- Update parameters
	- For HMM -\> Baum-Welch

![a b Statetransition probabilities, xo Erl Etl Gaus...](../../../../img/OneNote/Training%20image%200fd75709f75f6f27.png)  

- Make pass of all training sequences
- Gamma accumulator only evaluated once

![Forward compute likelihoods arti Backward compute ...](../../../../img/OneNote/Training%20image%2058863b5a0c9de381.png)

![Utterances thih sibs piytsh sh t iys z ih th Hlnit...](../../../../img/OneNote/Training%20image%20d2da868074e3d6c0.png)  

- Combine labelled with unlabelled data
	- Harder to get labelled data
- Allow weakly supervised, unlabelled data set to be more general
 
![Parallel procedure Transition likelihoods e ij a _...](../../../../img/OneNote/Training%20image%202b8ec48f5d54bbff.png) ![Repeat For all files in the training set I. recomp...](../../../../img/OneNote/Training%20image%20d510538baca5aacd.png)

- _Optimal representation of training data_
	- _Within constraints of model_
- _Iterative_
- _Incremental updates_
- _Local optimum_
