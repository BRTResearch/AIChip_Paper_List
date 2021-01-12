**Paper title:**

Duplo: Lifting Redundant Memory Accesses of Deep Neural Networks for GPU Tensor
Cores

**Publication:**

MICRO’2020

**Problem to solve:**

1.  Tensor cores augment the computational intensity of neural networks, but it
    has a critical drawback in that the convolution becomes memory-inefficient.
    Expanding input data during the lowering process inevitably generates
    multiple duplicates of the same data.

2.  Lowering the convolution increases the size of matrix to compute and
    requires correspondingly larger memory space to accommodate the expanded
    volume of data. It also exacerbates the number of memory transactions to
    load the duplicates of data that are stored at different memory addresses in
    the expanded workspace matrix.

**Major contribution:**

1.  The paper devise a GPU architecture named Duplo that minimizes redundant
    memory accesses of convolutions in DNNs attempting to load the duplicates of
    the same data.

2.  Using compile-time information, this paper establishes a cache-like
    mechanism to detect GPU access to main memory and redirect access.
