---
onenote-id: 0-fa35014189180c8a1ac994e5e863bd5a!1-D084F068F621FF9!3714
---
![POlA](../../../../img/OneNote/Likelihoods%20image%20c296fcc47c822180.png)  

- Marginalise state sequence by summing over all X
- Probability of observations by considering all possible states
 ![all](../../../../img/OneNote/Likelihoods%20image%20193e2ec0698c69c9.png)

- Same as above from 1 to T

Forward Likelihood
 ![Exported image](../../../../img/OneNote/Likelihoods%20image%20938640f285db446e.png)

- $𝛼$ for forward likelihood
	- Up to particular node in trellis
	- Co-ordinate in trellis
	- t across, j up
 
- All previous state sequences as long as finishes in state j at time t
 ![Qtj atli Pxt jlxtl i, Potlxt j,](../../../../img/OneNote/Likelihoods%20image%20fa0407b69520a747.png)  

Forward Procedure
 
- Calculate forward likelihoods
 ![1. Initialise at t 1 al i Tibi01 2,3,...,T, 2. Rec...](../../../../img/OneNote/Likelihoods%20image%202e130734eb7cf29d.png)  
![Exported image](../../../../img/OneNote/Likelihoods%20image%200ee826e5a3290a50.png)

- Operation 2, summing all to produce forward likelihood

Backward Procedure
 ![POT t 1 Ixt i,](../../../../img/OneNote/Likelihoods%20image%2028a88a845dea3ec4.png)

- From next observation (t+1) to end of sequence
 
- Gives same answer as forwards
- Useful for training
 ![1. 2. 3. Initialise at t T 3Ti Recur for t T 1, T ...](../../../../img/OneNote/Likelihoods%20image%207a0dcd537a9f8777.png)  
![Exported image](../../../../img/OneNote/Likelihoods%20image%2015c99d417c4879a5.png)

Best Path
 ![vlx](../../../../img/OneNote/Likelihoods%20image%20412b6fd5fc6bb7db.png)  

Viterbi Algorithm
 
Maximum Cumulative Likelihood
 ![tj max POI,](../../../../img/OneNote/Likelihoods%20image%20b0d6d9033ca60e71.png)

- Belongs to a node
- Similar to forward likelihood
	- Pick best route instead of calculating for all
- Don’t marginalise out states
 ![1. 2. 3. 4. Initialise at t 1 51 D TibiOI qli O 2,...](../../../../img/OneNote/Likelihoods%20image%20693a66c5a135a4ed.png)  
![Exported image](../../../../img/OneNote/Likelihoods%20image%2015abc17b60627d1d.png)  

- Pick best instead of adding up (max, argmax)

Which state came from

![1. 2. 3. 4. Initialise, Tibi01 tli O Recur for t 2...](../../../../img/OneNote/Likelihoods%20image%207e433a8184e1573a.png)

Log Probabilities
 
Multiplying loads of probabilities gets really small

- Underflow
 
Use log probabilities instead

- Wont degenerate down to 0
- Rank the same as non-log probabilities
 ![ln btot](../../../../img/OneNote/Likelihoods%20image%20c5ed94424e7fa212.png)  
![Q maxQX](../../../../img/OneNote/Likelihoods%20image%204aa06987ae7b5934.png)  
![Exported image](../../../../img/OneNote/Likelihoods%20image%20937b7dfc7587951c.png)   ![1. Initially at t 1 In 51 t In I n 01 VIi o 2,3,.....](../../../../img/OneNote/Likelihoods%20image%20ab221094b1d5d72c.png)  

State Transition

State Output
   
![state transition matrix 0 0 0.6 0.4 011 012 021 02...](../../../../img/OneNote/Likelihoods%20image%207e4b57c5afec9132.png)
