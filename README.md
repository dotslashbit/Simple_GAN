# Simple_GAN
This is an implementation of simple GAN with pytorch. This implementation is based on the following paper https://doi.org/10.48550/arXiv.1406.2661  


This is a new framework for estimating generative models via an adversarial process, in which we simultaneously train two models:  
- A generative model G that captures the data distribution.
- A discriminative model D that estimates the probability that a sample came from the training data rather than G.

The training procedure of G is to maximize the probability of D making a mistake.  
In the case where G and D are defined by multilayer perceptrons, the entire system can be trained with backpropagation.  

The generative model can be thought of as analogous to a team of counterfeiters,
trying to produce fake currency and use it without detection, while the discriminative model is
analogous to the police, trying to detect the counterfeit currency. Competition in this game drives
both teams to improve their methods until the counterfeits are indistiguishable from the genuine
articles.  

In this article, we explore the special case when the generative model generates samples
by passing random noise through a multilayer perceptron, and the discriminative model is also a
multilayer perceptron. We refer to this special case as adversarial nets. In this case, we can train
both models using only the highly successful backpropagation and dropout algorithms and
sample from the generative model using only forward propagation.  
