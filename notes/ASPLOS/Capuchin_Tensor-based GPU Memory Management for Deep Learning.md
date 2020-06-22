**Paper title:**

Capuchin: Tensor-based GPU Memory Management for Deep Learning

**Publication:**

ASPLOS’20

**Problem to solve:**

Since GPU global memory is a scarce resource, large models also pose a
significant challenge due to memory requirement in the training process. This
restriction limits the DNN architecture exploration flexibility. However, the
high-bandwidth GPU on-board memory is a scarce resource. The major memory
footprint in DNN training is due to intermediate layer outputs, i.e., feature
maps. These feature maps are produced in the forward propagation and used again
in the backward propagation. Thus, major deep learning frameworks usually
maintain these feature maps in GPU memory until they are no longer needed in
backward propagation computation. However, there is usually a large gap between
two accesses to the same feature map in forward and backward propagation, which
incurs high memory consumption to store the intermediate results.

Swapping and recomputing are two main techniques to reduce the memory footprint,
and existing works proposed layer-wised GPU memory management and rely on static
analysis. Layer-wise memory management is too coarse-grain to fully optimize the
memory usage, and static analysis failed to fit different hardware and
developing networks.

The paper aims to solve the GPU memory shortage problem in deep learning
training with fine-grain memory management and runtime tracking.

**Major contribution:**

The paper proposed Capuchin, a tensor-based GPU memory management module for
deep learning frameworks to reduce the memory footprint via **tensor**
eviction/prefetching and recomputation. The key feature of Capuchin is that it
makes memory management decisions based on tensor access pattern **tracked at
runtime** with a unique ID for each tensor.

The main contribution is as follow:

1.  Proposing a tensor-wise GPU memory management design. The management is
    based on tensors in the datafow execution model, and eviction/prefetching
    and recomputation methods are used to get the tensors ready when needed.

2.  Proposing runtime tensor tracking and access patterns analysis, and a
    flexible policy based on such analysis. The training process is composed of
    millions of iterations with clear boundaries, and the tensor accesses have
    regular and repeated access patterns across iterations.

3.  Implementing Capuchin on top of the widely used deep learning framework,
    Tensorflow and evaluating Capuchin on P100 GPU, showing that Capuchin can
    accommodate larger batch size compared to original Tensorflow, or achieves
    up to 3.86× speedup over vDNN.

Due to the regularity of tensor access pattern, the training are divided into
two phases: (1) measured execution: the execution of the first mini-batch
(iteration) from where the dynamic tensor access sequence, based on which tensor
memory management decisions can be made; and (2) guided execution: the training
process after the first iteration based on the memory management policy
generated using observed tensor access patterns.

The paper estimates swap and recomputation cost based on the profiling of access
time in measured execution. The policy and decision on which tensors should be
handled and which method should be used are discussed in detail.

**Lessons learnt:**

The paper proposed a fine-grained memory management system for tensors in deep
learning. The idea of using swap and regeneration is quite direct.

The cost only included time in the paper, but energy may be another important
cost to be further considered.
