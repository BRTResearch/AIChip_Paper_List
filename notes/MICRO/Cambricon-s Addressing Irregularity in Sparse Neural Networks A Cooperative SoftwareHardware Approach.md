**Paper title:**

Cambricon-S: Addressing Irregularity in Sparse Neural Networks: A Cooperative
Software/Hardware Approach.

**Publication:**

MICRO‘18

**Problem to solve:**

Neural networks keep moving towards deeper and larger architectures, posing a
great challenge to the huge amount of data and computations. Although sparsity
has emerged as an effective solution for reducing the intensity of computation
and memory accesses directly, irregularity caused by sparsity (including sparse
synapses and neurons) prevents accelerators from completely leveraging the
benefits; it also introduces costly indexing module in accelerators.

**Major contribution**

This paper proposes a cooperative software/hardware approach to address the
irregularity of sparse neural networks efficiently. Initially, we observe the
local convergence, namely larger weights tend to gather into small clusters
during training. Based on that key observation, we propose a software-based
coarse-grained pruning technique to reduce the irregularity of sparse synapses
drastically. The coarse-grained pruning technique, together with local
quantization, significantly reduces the size of indexes and improves the network
compression ratio. Paper further design a hardware accelerator, Cambricon-S, to
address the remaining irregularity of sparse synapses and neurons efficiently.
The novel accelerator features a selector module to filter unnecessary synapses
and neurons. Compared with a state-of-the-art sparse neural network accelerator,
the accelerator is 1.71× and 1.37× better in terms of performance and energy
efficiency, respectively.
