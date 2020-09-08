**Paper title:**

Manna An Accelerator for Memory-Augmented Neural Networks

**Publication:**

MICRO’19

**Problem to solve:**

Memory-augmented neural networks (MANNs) present a unique challenge due to soft
reads and writes to the differentiable memory, each of which requires access to
all the memory locations. This results in poor performance of MANNs on modern
CPUs, GPUs, and other accelerators.

**Major Contributions:**

1.  Provide a detailed investigation of the computational characteristics of
    MANNs, a promising emerging class of DNNs.

2.  Propose Manna, an end-to-end, CMOS-based accelerator that is able to
    efficiently perform all kernels used in memory augmented neural networks. We
    provision Manna with a memory-to-compute resource allocation reflective of
    the low FLOPs/Byte inherent to MANNs.

3.  Implement a hardware-based transpose mechanism to efficiently execute both
    vector-matrix and vector-transposed matrix multiplications.

4.  Provision Manna with specialized units (called eMACs), which are designed
    for the unique mix of operations beyond just MACs that are used in MANNs.

5.  Develop an ISA and compiler that map MANNs to Manna so as to minimize data
    transfers and maximize the utilization of on-chip bandwidth.

6.  Develop an architectural simulator and synthesize RTL implementations of key
    components in order to demonstrate the benefits of Manna. Our experiments
    indicate that Manna achieves average speedups of 39x (24x) and average
    energy improvements of 122x (86x) over an NVIDIA 1080-Ti (2080-Ti) GPU with
    a Pascal (Turing) architecture.
