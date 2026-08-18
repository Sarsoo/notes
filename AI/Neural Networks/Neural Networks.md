---
title: 'Neural Networks'
tags:
  - ai
---
- Massively parallel, distributed processor
- Natural propensity for storing experiential knowledge

# Resembles Brain

- Knowledge acquired from by network through learning
- Interneuron connection strengths store acquired knowledge
	- Synaptic weights

![slp-arch](../../img/slp-arch.png)

A neural network is a directed graph consisting of nodes with interconnecting synaptic and activation links, and is characterised by four properties

1. Each neuron is represented by a set of linear synaptic links, an externally applied bias, and a possibly nonlinear activation link. The bias is represented by a synaptic link connected to an input fixed at +1
2. The synaptic links of a neuron weight their respective input signals
3. The weighted sum of the input signals defines the induced local field of the neuron in question
4. The activation link squashes the induced local field of the neuron to produce an output

# Why Extract Classical Rules from Neural Nets
- Allows understandable external validation by users
- Improve generalisation performance
	- Identifying input space where training data not represented
	- Identifying times when net may fail to generalise
- Discover salient features for exploration
- Interface bittern connectionist and symbolic approaches to development
- Validation for safety requirements