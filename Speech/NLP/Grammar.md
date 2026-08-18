---
onenote-id: 0-4e0dad4f7dc1060d3d8ddef1daf83c6d!1-D084F068F621FF9!3707
---
# Isolated Word Recognizer
- Data prep
- Training
- Testing
- Analysis
 
[Markov Models](../../../../../../AI/Pattern%20Matching/Markov/Markov.md)
 ![V ectors](../../../../img/OneNote/Grammar%20image%2060f9e3c33535bf24.png)    
$$\hat{w}=\arg\max_i\{P(w_i|\mathcal{O})\}$$
$$P(w_i|\mathcal{O})=\frac
{P(\mathcal{O}|w_i)P(w_i)}
{P(\mathcal{O})}$$
![Exported image](../../../../img/OneNote/Grammar%20image%20f48b5b0ce7322d55.png)  
![Unknown 1 2 Choose 0](../../../../img/OneNote/Grammar%20image%205adaf640ad0f8dab.png)

# Performance
- Substitution, S
- Deletion, D
- Insertion, I
 ![Correct 100 Accuracy 100 Error rate 100 x x x](../../../../img/OneNote/Grammar%20image%208f6abc4e6d7bce99.png)

- N = length of sequence

# Binary Grammar Example
- Yes or No
 ![Machine generated alternative text yes no](../../../../img/OneNote/Grammar%20image%20b75a8d6348ee9637.png)  
![Machine generated alternative text answer YES I NO...](../../../../img/OneNote/Grammar%20image%20f1c717b7734f8018.png)  
![yes](../../../../img/OneNote/Grammar%20image%2007b7a01fa7b6758e.png)

# Connected Digit Grammar Example
- Variable length series of numbers
 ![Machine generated alternative text one two zero](../../../../img/OneNote/Grammar%20image%20545b5e47bed536ad.png)

- Loopback for connected digits
 ![Machine generated alternative text digit ONE I TWO...](../../../../img/OneNote/Grammar%20image%205a03de9580a53567.png)

- Angle brackets for one or series
 ![two one](../../../../img/OneNote/Grammar%20image%204917be03adaa3738.png)

- Model transitions not made at frame
	- In-between

![Machine generated alternative text a one two zero ...](../../../../img/OneNote/Grammar%20image%20ab61ed01d9e17d2b.png)

# Context Free Grammars
- Common phrases/sequences
- Can be described simply
- Answers for forms
 ![Sunda Monda Wednesd a Ihursda Frida Saturda 2nd 30...](../../../../img/OneNote/Grammar%20image%20bb9b8bcc31a14a67.png)

Use phonemes instead for flexibility
 ![Word level Network level HMM level Recognition net...](../../../../img/OneNote/Grammar%20image%2084448b3cb5a83971.png)  
![need the dh on ay of ax n aa ay](../../../../img/OneNote/Grammar%20image%205a8623a432504553.png)  

# Null States
- Beginning and end of model
- Don't generate observations
- Align given model with test
- Joining words in grammar
	- Use transitions to model language
 ![Exported image](../../../../img/OneNote/Grammar%20image%2046e52c09bd9851a9.png)  

Isolated Word Recognition
 ![digit ONE I TWO I THREE I FOUR I FIVE I SIX I SEVE...](../../../../img/OneNote/Grammar%20image%20b03dc269cda3aa78.png)   
![Machine generated alternative text one two zero Gr...](../../../../img/OneNote/Grammar%20image%20e1f1f54640d66482.png)  ![Best Token came Recording Decisions Before 10 P 10...](../../../../img/OneNote/Grammar%20image%2039b8ec4dd192cef1.png)

