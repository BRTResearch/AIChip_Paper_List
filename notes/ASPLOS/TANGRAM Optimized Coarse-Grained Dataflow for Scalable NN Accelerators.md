**Paper title:**

TANGRAM: Optimized Coarse-Grained Dataflow for Scalable NN Accelerators.

**Publication:**

ASPLOS’19

**Problem to solve:**

To get scalable performance on tiled accelerators, we must optimize the
coarse-grained parallelism across multiple tiles, in addition to the
fine-grained parallelism within each engine. However, existing dataflow schemes
for coarse-grained parallelism suffer from significant inefficiencies. a)
Parallelizing a single NN layer (intra-layer parallelism) leads to significant
data duplication, and b) pipelining the processing of multiple layers
(inter-layer pipelining) results in substantial challenges in resource
utilization and on-chip buffer requirements. These problems need to be solved.

**Major contribution:**

Its primary contribution is the optimized dataflow.

1.  For intra-layer parallelism, the authors develop buffer sharing dataflow
    (BSD) that eliminates the inefficiencies resulted from data duplication in
    on-chip buffers. It effectively turns the distributed SRAM buffers into an
    idealized shared buffer that always has the necessary data close to the
    processing tile. In effect, BSD solves the problem a).

2.  For inter-layer pipelining, Tangram introduces alternate layer loop ordering
    (ALLO) dataflow to forward intermediate fmap data in a more fine-grained and
    timely manner, which reduces the on-chip buffering requirements and the
    pipeline filling/draining delays. ALLO actually solves the problem b).

3.  At present, more and more networks have complex DAG structures (resnet,
    googlenet, LSTM, etc.). Therefore, this paper optimizes the allocation
    strategy for this complex network, which can minimize the number of complex
    data dependencies served through the off-chip memory.

**Lessons learnt:**

Tangram’s implementation includes two parts: 1) a search tool that identifies
the optimized parallelization schemes for each NN; 2) a compiler that produces
the code for the selected schemes.
