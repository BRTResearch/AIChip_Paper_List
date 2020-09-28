**Paper title:**

Tensaurus: A Versatile Accelerator for Mixed Sparse-Dense Tensor Computations

**Publication:**

HPCA’20

**Problem to solve:**

Tensor factorizations have traditionally been used in recommender systems to
produce factor matrices that represent an embedding into the reduced latent
space. But there are two key challenges with designing an accelerator for tensor
factorizations. First, many of the real-world tensors are sparse, which makes
tensor factorizations memory bound. Second, the compute and memory access
patterns of different tensor factorizations can be very different, which makes
it necessary to reduce these computations into some basic operations and
implement them in the hardware.

**Major contribution:**

To tackle above problem, the paper proposes a new hardware accelerator for
highly efficient processing of mixed sparse and dense tensor computations. The
contributions are as follows:

1.  First to propose a hardware accelerator that is capable of accelerating not
    only sparse tensor factorizations, but also dense tensor factorizations and
    other common mixed sparse-dense (sparse-dense and dense-dense) matrix
    operations for a wide range of sparsity.

2.  Introduce a new sparse storage format, *compressed interleaved sparse slice*
    (*CISS*), which allows accessing sparse data in a vectorized and streaming
    manner and thus achieves high memory bandwidth utilization and performance
    for sparse tensor kernels.

**Lessons learnt:**

Better performance is often achieved when hardware and software are designed
together. By this mean, the authors achieve significant speedup and energy
reduction for tensor factorizations over the state-of-the-art CPU and GPU
implementations.
