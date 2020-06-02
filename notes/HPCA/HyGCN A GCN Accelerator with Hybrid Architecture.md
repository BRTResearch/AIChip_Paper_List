**Paper title:**

HyGCN: A GCN Accelerator with Hybrid Architecture

**Publication:**

HPCA’20

**Problem to solve:**

The hybrid execution patterns of GCNs (graph convolutional neural networks)
require a design that alleviates irregularity and exploits regularity. To
achieve higher performance and energy efficiency, the design needs to leverage
the high intra-vertex parallelism in Aggregation phase, the highly reusable
inter-vertex data in Combination phase, and the opportunity to fuse
phase-by-phase execution introduced by the new features of GCNs. Existing
architectures fail to implement GCN-specific characteristics. They are not the
ideal platforms to execute GCNs.

1.  For CPUs, they fail to address the abundant dynamic and irregular data
    accesses in the Aggregation phase. Besides, it is difficult to efficiently
    implement the reuse of the highly reusable parameter data between computing
    units.

2.  For GPUs, they lack the ability to alleviate irregularity in Aggregation
    phase. Futhermore, the data copy and synchronization between threads for the
    parameter reuse are expensive.

3.  For graph analytics and neural network accelerators, they are only optimized
    to alleviate irregularity or exploit regularity, rather than both
    simultaneously.

4.  All of them are short of the ability to efficiently fuse the execution of
    these two phases.

**Major contribution:**

1.  Study an emerging domain, GCNs, from a computer architecture perspective and
    show that hybrid execution patterns exist in GCNs. Specially, the
    Aggregation phase in GCNs presents a dynamic and irregular execution
    pattern, while Combination phase is static and regular.

2.  Propose a GCN accelerator, HyGCN, using a hybrid architecture to efficiently
    perform GCNs. First, build a programming model to enable the hardware design
    to exploit various parallelisms inherent in this domain. Next, propose a
    hardware design to tackle irregularity and leverage regularity with
    Aggregation Engine and Combination Engine, respectively.

3.  Propose a flexible inter-engine pipeline and a priority-based memory access
    coordination to efficiently fuse the execution of Aggregation phase and
    Combination phase.

4.  Implement our architecture design in RTL and evaluate it using a detailed
    micro-architectural simulation. Use four well-known GCN models on six
    popular graph datasets. Compared to the state-of-the-art software framework
    PyTorch Geometric running on Intel Xeon CPU and NVIDIA V100 GPU, our work
    achieves on average 1509x speedup with 2500x energy reduction and 6.5x
    speedup with 10x energy reduction, respectively.
