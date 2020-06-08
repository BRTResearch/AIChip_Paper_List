**Paper title:**

GraphR: Accelerating Graph Processing Using ReRAM

**Publication:**

HPCA’18

**Problem to solve:**

Due to the large-scale spectrum of graph application, graph is a hot-point
direction, worthy of taking into account for many researchers. While the graph
processing is faced with the poor locality and high memory bandwidth
requirement, this paper is willing to architect an accelerator to ameliorate
these bottlenecks.

**Major contribution:**

1.  This paper demonstrates that the ReRAM could serve as the essential hardware
    building block to perform matrix-vector multiplications in graph processing.
    While there are some challenges that need solving, such as data
    representation, large graph, execution model and algorithm mapping.

2.  This paper proposed a novel ReRAM-based accelerator-GraphR, for graph
    processing. Memory ReRAM and graph engine (GE) are main parts of the
    accelerator, memory ReRAM for storing graph data in CSR format and GE for
    performing the matrix-vector multiplication on the sparse matrix
    representation.

3.  This paper also proposed two algorithm mapping patterns, parallel MAC and
    parallel add-op, to achieve good parallelism for diverse algorithms.

4.  This paper evaluated the speedup and energy-efficiency of GraphR. Compared
    with CPU baseline, GraphR achieves a 10.01x(up to 132.67x) speedup and a
    33.82x energy saving, 1.69x to 2.19x speedup and 4.77x to 8.91x energy
    saving for GPU, 1.16x to 4.12x speedup and 3.67x to 10.96x energy saving for
    PIM-based architecture.

**Lessons learnt:**

1.  If an application has large data to process, just repeating a lot of similar
    operation, the ReRAM may be a good idea to be adopt to design the
    architecture. To be clearly speaking, the ReRAM is suitable for the
    application resilient to errors.

2.  Blocking is a fantastic way to resolve a lot of sophisticated application.
    Memory block can reduce the data movement and enhance the locality, while
    computation block can exhibit the flexibility and parallelism concurrently.
    Managing the block is a key for the mid-point between performance and cost.
