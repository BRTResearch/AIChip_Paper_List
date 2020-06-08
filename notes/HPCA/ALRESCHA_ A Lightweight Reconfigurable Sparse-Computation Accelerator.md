**Paper title:**

ALRESCHA: A Lightweight Reconfigurable Sparse-Computation Accelerator

**Publication:**

HPCA’20

**Problem to solve:**

The parallelism and data dependency problem in sparse computation workloads.

**Major contribution:**

1.  Proposed a generic sparse accelerator for both scientific calculations and
    graph calculations regardless of whether they have data-dependent patterns.

2.  To support the accelerator mentioned above, this paper proposed a
    lightweight reconfigurability method, which reconfigures the part of the
    accelerator runtime.

3.  To support the whole method, this paper proposed a storage format to stream
    data and facilitate the computations with data-dependency.

**Lessons learnt:**

1.  This paper actually composes the methods in two kinds of accelerators: GEMV
    computation accelerator and graph computation accelerator. However, the
    implementation of fast runtime switch between configurations in RCU is still
    valuable.

2.  The GEMV accelerator part proposed by this paper is not much innovative,
    while the most innovative part is the storage part. This kind of format
    helps the graph computations most.
