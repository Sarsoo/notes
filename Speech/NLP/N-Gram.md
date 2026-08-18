---
onenote-id: 0-b398c160d9570dfe1c3315204ffc5402!1-D084F068F621FF9!3707
---
# Bigram
 $$P\left(w_k|w_1^{k-1}\right)\approx P\left(w_k|w_{k-1}\right)$$

- Approximate word sequence to just last word as context
$$P(w_1^n)=\prod_{k=1}^nP(w_k|w_{k-1})$$
 $$\begin{align}
 P(w_k|w_{k-1}) &= \frac
 {C\left(w_{k-1}w_k\right)}
 {\sum_{\mathfrak{K}\in V}C\left(w_{k-1}w_{\mathfrak{K}}\right)}\\\\
 &= \frac
 {C(w_{k-1}w_k)}
 {C(w_{k-1})}
 \end{align}$$
- Numerator, count of word pairs
- Denominator, all pairs with prior word as context
	- Simplifies to just the frequency of the _context_ word  
# Extend to N-Grams
$$P(w_k|w_{k-N+1}^{k-1})=\frac
{C(w_{k-N+1}^{k})}
{C(w_{k-N+1}^{k-1})}$$
# Berkeley Restaurant Project
- Matrix of word pair frequencies
	- Turn into probabilities
- Unheard pairs in the training data become illegal

# Laplace Add-One Smoothing
- Any illegal word pairs will be a x 0 and zero the whole string
- Make minimum pair count 1 to allow _novel utterances_
$$C^*(w)=C(w)+1$$
$$P^*(w_k|w_{k-1})=\frac
{C(w_{k-1}w_k)+1}
{C(w_{k-1})+V}
$$
  
![i want i want want 827 want 828 to 608 to 609 eat ...](../../../../img/OneNote/N-Gram%20image%20dbe2361d6c2ce3a3.png)
- Crude, distorts data quite a lot

# Witten-Bell Discounting
$$P^*(w_{unseen})\approx\frac{T}{N}=\frac{\#type}{\#word}$$
- T is effectively vocabulary
- N includes repetitions
- Estimate probability of unseen word

# Good-Turing Discounting
$$
\begin{align}
P^*_0 &= \frac{n_1}{N} \\
P^*_r &= (1-P^*_0)\frac{k_r}{N^*} \\
\mathrm{where} \space k_r &= (r + 1)\frac{n_r+1}{n_r}
\end{align}
$$
- Use number of repetitions of certain words

# Backoff
- Increasing order increases parameters
- Lots of holes to fill
- Trade-off between
	- Detail and precision of high order
	- Reliability of low-order
$$P^*(w_3|w_1,w_2)\approx\hat{P}(w_3|w_2)$$
- If can't estimate tri-gram
	- Use bi-gram instead
 ![1 PWI Pwv PWI IWI PWI IWW zerogram unigram bigram ...](../../../../img/OneNote/N-Gram%20image%20de5c998af82d32f7.png)
- Increasing order increases knowledge of vocabulary

# Deleted Interpolation
- Use weighted average of different orders
- Continuous version, almost, of back-off
$$P^*(w_3|w_1,w_2)=a_3\hat{P}(w_3|w_1,w_2)+a_2\hat{P}(w_3|w_2)+a_1\hat{P}(w_3)+a_0\frac{1}{V}$$

# Language Modelling
 $$\hat{W}=\arg \max{}_W\quad \underbrace{P(\mathcal{O}|W)}_{acoustic\space model}\quad \underbrace{P(W)}_{langauge\space model}$$
 $$
 \begin{align}
 P(w_1^n) &= P(w_1)P(w_2|w_1)P(w_3|w_1^2) \dots P(w_n|w_1^{n-1}) \\
 &= \prod^n_{k=1}P(w_k|w_1^{k-1})
 \end{align}
 $$   
- Initial assumption
	- Free words of context
	- Independent
$$P(w_k|w_1^{k-1})\approx P(w_k)$$
$$P(w_k)=\frac{C(w_k)}{n}$$
- Count of word over amount of words
	- Basic likelihoods
 
- Discard word order, phrasing, context
 
- Model full context
$$\mathcal{O}(\mathrm{I\space saw\space two\space rabbits})=\mathcal{O}(V)+\mathcal{O}(V^2)+\mathcal{O}(V^3)+\mathcal{O}(V^4)$$
	- Parameters grow exponentially

# N-Grams
$$P(w_k|w_1^{k-1})\approx P(w_k|w_{k-2}^{k-1})$$
$$P(w_k|w_1^{k-1})\approx P(w_k|w_{k-3}^{k-1})$$
$$P(w_k|w_1^{k-1})\approx P(w_k|w_{k-N+1}^{k-1})$$
# Evaluating Models
- Perplexity
	- Bad on its own
		- Use extrinsic evaluation
		- Unless test looks like training
	- Entropy
	- Bits
$$H(W)=-\sum_{w\in \mathcal{V}}P(w)\log_2P(w)$$
# Cross-Entropy

Between model,  
, and test sequence,  
$$H(W,m)=\lim_{n\rightarrow\infty}-\frac{1}{n}\log_2P(w_1^n|m)$$  
$$\mathrm{where}\space P(w_1^n|m)=\prod^N_{n=1}P(w_n|w_1^{n-1})$$
- Limit as the word length increases to infinity
- Geometric mean
	- Average log probability
 
- Perplexity
	- Log of each other
$$PP(W)=2^{H(W)}$$
$$\mathrm{where}\space PP(W)=N\sqrt{\prod_{n=1}^N\frac
{1}
{P(w_n|w_1^{n-1})}
}$$
 
![Machine generated alternative text Bigram probabil...](../../../../img/OneNote/N-Gram%20image%20400662c1d4967f7e.png)  

- Big values affected more than mid values
