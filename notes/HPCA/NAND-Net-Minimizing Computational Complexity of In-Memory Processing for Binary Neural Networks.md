**Paper title:**

NAND-Net: Minimizing Computational Complexity of In-Memory Processing for Binary
Neural Networks

**Publication:**

HPCA’19

**Problem to solve:**

Memory bottlenecks are continuously along with the current DL technologies,
degrading the energy-saving with regard to mobile device. As such, binary neural
networks (BNN) come out as an emerging scheme to alleviate these bottlenecks.
However, prior conventional memory architectures hamper the performance of BNN
by incurring overhead. Naturally, it is necessary to devise a new architecture
for memory suited to BNN.

**Major contribution:**

This paper proposed NANDNet, an efficient architecture to minimize the
computational complexity of in-memory processing for BNNs. It decomposed each
convolution into sub-convolutions and eliminated the unnecessary operations
based on redundancies contained in BNNs. For the remaining convolution, use
bitwise NAND operation to replace them. This paper demonstrated that the NANDNet
yields a 1.04-2.4x speedup and 34-59% energy-saving via the evaluation, thus
making it a suitable solution to implement efficient in-memory processing for
BNN.

**Lessons learnt:**

There may be a large design space for BNN when considering the architecture
designing and break through the bottleneck of performance. BNN works with the
binary bits to achieve the function of other NN, with few conversions of data
format. Therefore, this computation type facilitates BNN with hardware-friendly
feature, reducing the complexity from the point of view in hardware.
