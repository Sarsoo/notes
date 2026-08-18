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

# Knowledge Representation Rules
1. Similar inputs from similar classes should usually produce similar network representations
	- Should be classified same
	- Similarity can be
		- Euclidean
		- Dot product
2. Inputs from different classes should give different network representations
	- Opposite of 1
3. Important features should have regions of neurons representing it
	- Large numbers of neurons increases accuracy
	- Tolerates faulty neurons
4. Prior information should be built into network in order not to learn it
	- Simplifies design
	- Specialised structure has less free parameters
		- Smaller training set needed
		- Learns faster
		- Generalises better

