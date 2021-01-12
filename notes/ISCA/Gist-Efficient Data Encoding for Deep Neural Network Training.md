**Paper title:**

Gist-Efficient Data Encoding for Deep Neural Network Training

**Publication:**

ISCA’18

**Problem to solve:**

1.  The memory of GPUs is becoming the bottleneck for DNNs to get deeper.

2.  Prior approaches to reduce the memory footprint are not able to
    simultaneously achieve all of the following three desirable
    properties:(1)provide high memory footprint reduction, (2) low-performance
    overhead, (3) minimal effect on training accuracy.

3.  The stashed feature maps (generated in the forward and used in both forward
    and backward passes) and immediately consumed data structures consume the
    large part of memory.

**Major contribution:**

The previous works focuses on the reduce of number of layers or the size of
minibatch. But these methods are inefficient and do harm to the accuracy. The
author finds that the stashed feature maps and immediately consumed data cost
most of memory, so they propose a kind of memory saving method by analyzing the
type of layers to use different kinds of method to encode feature maps, and
decode when they needed.

1.  A systematic memory footprint analysis is used, and shows that feature maps
    are the major memory consumers in the DNN training process. Among feature
    maps, there is high data redundancy and it can be stored in much more
    efficient formants between their forward and backward use.

2.  Two kinds of layer-specific encodings are proposed. One is binarize that
    achieves 32X compression for ReLU outputs for layer combination of ReLU
    followed by Pool. The other is sparse storage and dense compute, which
    exploits high sparsity exhibited in ReLU outputs for ReLU followed by
    convolution layers.

3.  DPR, that applies precision reduction only for the backward use of the
    feature maps – values in the forward pass are kept in full precision –
    leading to aggressive bit savings without affecting accuracy.

4.  By reducing memory footprint, Gist can fit larger minibatches in the GPU
    memory, improving GPU utilization and speeding up the training for very deep
    networks
