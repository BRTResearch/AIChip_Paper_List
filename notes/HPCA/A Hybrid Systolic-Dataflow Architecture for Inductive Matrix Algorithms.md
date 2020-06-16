**Paper title:**

A Hybrid Systolic-Dataflow Architecture for Inductive Matrix Algorithms

**Publication:**

HPCA’20

**Problem to solve:**

1.  In some dense linear algebra kernels, the inductive nature make parallelism
    difficult to exploit: parallel regions have fine-grain producer/consumer
    interaction with iteratively changing dependence distance, reuse rate, and
    memory access patterns.

2.  High overhead both for multi-threading due to fine-grain synchronization,
    and for vectorization due to the nonrectangular iteration domains, as a
    result, CPUs, DSPs, and GPUs perform order-of-magnitude below peak.

3.  Find a way to execute parallel code regions in the above kernels
    efficiently.

**Major contribution:**

1.  Identification of fine-grain inductive behavior for many dense linear
    algebra kernels.

2.  Propose an inductive dataflow execution model which expresses inductive
    memory and dependences as a first-class primitive to reduce control overhead
    and make vectorization profitable.

3.  A novel hybrid systolic-dataflow architecture to specialize for the exposed
    inductive parallelism.

4.  REVEL accelerator design and its novel vector-stream control model which
    amortizes control in time and space.

**Lessons learnt:**

Like other similar paper in dataflow and architecture, this paper exploits the
connections of data (data have dependencies or other links in inner loop and
outer loop) in certain pattern, and design the accelerator for this kind of
dataflow. In past few years, dataflows in AI have been widely researched, and
this paper turns its eye to signal processing which is related to arising areas
like 5G.
