**Paper title:**

Diffy: a Deja vu-Free Differential Deep Neural Network Accelerator

**Publication:**

MICRO’18

**Problem to solve:**

Modern deep neural networks have great amount of computation and date transfer,
and many accelerators target on such high computational and data supply demands.
Taking advantage of the computation structure, the data reuse, the static and
dynamic ineffectual value content, and the precision requirements of DNNs, the
target of this paper is to build a accelerator minimizing the computation and
data transfer of DNNs without losing accuracy.

**Major contribution:**

1.  Experimentally shows that DNNs for Computational Imaging exhibit high
    spatial correlation in their runtime-calculated value stream.

2.  Presenting Diffy, a practical hardware accelerator that exploits this
    spatial correlation to transparently reduce the number of bits needed to
    store the network’s values on- and off-chip, and the computations that need
    to be performed.

The paper first analyses the information entropy of activations and conditional
entropy of activation knowing adjacent prefix activations along x axis, and the
entropy of delta between activations and adjacent prefix, showing that using
delta encoding can efficiently compress the activations both in on-chip and
off-chip.

Further, the paper propose a computing methods for convolution layers using
delta values of input feature maps, based on the Bit-Pragmatic accelerator,
which process activations “bit”-serially, one effectual term at a time in
modified Booth encoding. The paper shows that delta values have less effectual
terms than original activations, resulting in speeds up in computation.

Finally the paper experimentally study some typical DNNs to evaluation the
proposed accelerator architecture, achieving significant performance improving.

**Lessons learnt:**

It is possible to achieve lossless compression and computation speed up in DNNs.
Delta encoding is one of the simplest encoding, but it can be used in computing
unit, and achieved significant improvement. It may be possible to introduce
other lossless or lossy encoding methods and corresponding computation units,
and achieve more improvement.

The paper uses Bit-Pragmatic computation architecture, which can take adventure
of delta encoding, e.g. less effectual term in encoded activations. Without such
methods the computation speedup can’t be achieved.
