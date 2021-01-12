**Paper title:**

SAVE: Sparsity-Aware Vector Engine for Accelerating DNN Training and Inference
on CPUs

**Publication:**

MICRO’2020

**Problem to solve:**

1.  The sparsity in General Matrix Multiplication (GEMM) for DNN can be
    exploited to accelerate the training and/or inference. In DNNs, sparsity is
    often unstructured, which is a challenge for acceleration. Existing
    solutions often lower the accuracy of the model.

2.  Directly skipping zero in Vector Processing Units (VPU) doesn’t improve the
    performance since vector instruction still has to wait for other lanes to
    compute.

**Major contributions:**

1.  Proposed *SAVE*, which is a hardware adding to search through the operands
    pending in VPU reservation stations and schedule the vector lanes.

2.  Design hardware-efficient mechanisms to load-balance VPU lanes and added a
    small high-bandwidth cache to exploit locality and improve broadcast
    throughput and devised techniques to handle the complications from mixed
    precision VFMAs.

3.  *SAVE* is the first CPU vector pipeline that exploits unstructured sparsity
    and is transparent to software.

4.  Proposed some enhanced technique to improve the performance: Broadcast
    Cache; The Rotate-Vertical Coalescing Scheme; The Lane-Wise Dependence
    Scheme.

5.  Proposed solution for mix-precision cases.
