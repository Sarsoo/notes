- Massively parallel, distributed processor
- Natural propensity for storing experiential knowledge

# Resembles Brain

- Knowledge acquired from by network through learning
- Interneuron connection strengths store acquired knowledge
	- Synaptic weights

![[slp-arch.png]]

A neural network is a directed graph consisting of nodes with interconnecting synaptic and activation links, and is characterised by four properties

1. Each neuron is represented by a set of linear synaptic links, an externally applied bias, and a possibly nonlinear activation link. The bias is represented by a synaptic link connected to an input fixed at +1
2. The synaptic links of a neuron weight their respective input signals
3. The weighted sum of the input signals defines the induced local field of the neuron in question
4. The activation link squashes the induced local field of the neuron to produce an output

# Knowledge

*Knowledge refers to stored information or models used by a person or machine to interpret, predict, and appropriately respond to the outside world*

Made up of:
1. The known world state
	- Represented by facts about what is and what has been known
	- Prior information
2. Observations of the world
	- Usually inherently noisy
	- Measurement error
	- Pool of information used to train

- Can be labelled or not
	- (Un-)Supervised

*Knowledge representation of the surrounding environment is defined by the values taken on by the free parameters of the network*
- Synaptic weights and biases