**Paper title:**

Bit Prudent In-Cache Acceleration of Deep Convolutional Neural Networks

**Publication:**

HPCA’19

**Problem to solve:**

Numerous accelerators have been developed to achieve better latency, energy
efficiency, and throughput for CNN workloads. Specifically, weight pruning and
low precision are two popular approaches for neural network compression.
However, Neural Cache architecture is unaware of the redundancy in neural
networks. This paper poses the question: how can memory-centric architectures,
such as Neural Cache, benefit from removing the redundancy in CNN computation?

**Major contribution**

Develop techniques to leverage redundancy prevalent in DNNs for memory-centric
vector architectures such as Neural Cache. Redundancy can be eliminated by
pruning weights or using lower precision.

Analyze inefficiencies of convolution with pruned sparse models, and propose
novel techniques to enable dense computation amenable for vector processing with
sparse DNN models. Specifically, this paper explores a pruning method to
coalesce non-zero filter channels and develop a hardware block that dynamically
coalesces the input activations to align them with pruned weights.

Develop a pruning method for overlapping multiple filters together to
effectively utilize the vector units. This method does not require input
coalescing at runtime.

Design new bit-serial in-SRAM compute algorithms to exploit the ultra-low
precision binary and ternary network models. Convolutions with ternary/binary
weights are converted to logical operations and additions.

The evaluated sparsity-aware architecture achieves a 17.7×, 3.7×, 1.6× speedup
over server-class CPU, GPU, and Neural Cache baselines without accuracy loss; in
terms of energy efficiency, the design is 34.0×, 13.8×, 1.6× better than CPU,
GPU, and Neural Cache. We further show that with accuracy loss allowed, the
low-precision architecture has a latency 43.6×, 9.1×, 3.9× better than CPU, GPU,
and Neural Cache.
