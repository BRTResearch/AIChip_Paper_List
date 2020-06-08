**Paper title:**

CirCNN: Accelerating and Compressing Deep Neural Networks Using Block-Circulant
Weight Matrices

**Publication:**

MICRO’17

**Problem to solve:**

The widely used weight pruning achieves good compression ratios but suffers from
three drawbacks: 1) the irregular network structure after pruning, which affects
performance and throughput; 2) the increased training complexity; and 3) the
lack of rigorous guarantee of compression ratio and inference accuracy. The
paper aims to propose a methods to reduce the weights and speedup the
computation both in training and inference while guarantying accuracy.

**Major contribution:**

The paper’s main contribution is as follow:

1.  Propose block-circulant matrices, a type of structured matrices that values
    are circulant in blocks, to serve as the weights of neural networks.
    Block-circulant matrices have parameters far less than usual unstructured
    weight matrices used in ordinary neural networks, reducing storage
    complexity from O(n\^2) to O(n log n). The effectiveness, i.e. the universal
    approximation property, of block-circulant matrix-based neural networks are
    proved theoretically.

2.  Propose an accelerated computation methods for network layers using
    block-circulant matrices based on FFT, reducing computational complexity
    from O(n\^2) to O(n log n).

3.  Propose CirCNN architecture, a universal DNN inference engine that can be
    implemented in various hardware/software platforms with configurable network
    architecture, based on proposed block-circulant matrix-based algorithms.
    CirCNN architecture is tested in three platforms: FPGA, ASIC and embedded
    processors, showing that CirCNN architecture achieves very high energy
    efficiency and performance with a small hardware footprint.

It is worth noticing that no conversion methods between the unstructured weight
matrices and block-circulant matrices are provided, the network using
block-circulant matrices should be trained from scratch.

**Lessons learnt:**

Although structural weight pruning is also developing, this paper shows the
possibility of designing a class of neural networks with structural weights
(thus highly compressible) from the beginning.

The well-known FFT algorithms are extended to do calculations for
block-circulant matrices.

However, the paper only evaluated their proposed neural network layers on rather
simple dataset and network architecture, i.e. MNIST, SVHN, CIFAR-10, and
ImageNet datasets (compared to AlexNet).
