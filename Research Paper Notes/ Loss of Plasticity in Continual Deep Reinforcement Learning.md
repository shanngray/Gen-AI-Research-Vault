# Loss of Plasticity in Continual Deep Reinforcement Learning

## My Thoughts
The article introduces a new learning algorithm they call continual backpropogation. It differs from traditional backpropogation by adding a loss component that reintialises a subset of less-used parameters. This allows the network to continue learning passed the point where a tradtional NN would begin to degrade due to over training.

I find it interesting that the continual backpropogation mimics placticity in biological brains by incorporating elements of the decay of neurons that are under utilised as well as the growth of new neurons (i.e. reinitialising a parameter can be seen as analagous to a neuron dying and being replaced).

### Internal Links
[Backpropagation](./Terminology & Concepts/Backpropagation.md)

## Research Paper
[Loss of Plasticity in Continual Deep Reinforcement Learning](https://arxiv.org/abs/2303.07507)
[Dohare, S., Hernandez-Garcia, J.F., Lan, Q. et al. Loss of plasticity in deep continual learning. Nature 632, 768–774 (2024). https://doi.org/10.1038/s41586-024-07711-7](https://www.nature.com/articles/s41586-024-07711-7)

### Summary
The ability to learn continually is essential in a complex and changing world. In this paper, we characterize the behavior of canonical value-based deep reinforcement learning (RL) approaches under varying degrees of non-stationarity. In particular, we demonstrate that deep RL agents lose their ability to learn good policies when they cycle through a sequence of Atari 2600 games. This phenomenon is alluded to in prior work under various guises -- e.g., loss of plasticity, implicit under-parameterization, primacy bias, and capacity loss. We investigate this phenomenon closely at scale and analyze how the weights, gradients, and activations change over time in several experiments with varying dimensions (e.g., similarity between games, number of games, number of frames per game), with some experiments spanning 50 days and 2 billion environment interactions. Our analysis shows that the activation footprint of the network becomes sparser, contributing to the diminishing gradients. We investigate a remarkably simple mitigation strategy -- Concatenated ReLUs (CReLUs) activation function -- and demonstrate its effectiveness in facilitating continual learning in a changing environment.