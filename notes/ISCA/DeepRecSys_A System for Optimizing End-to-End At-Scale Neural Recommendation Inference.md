**Paper title:**

DeepRecSys: A System for Optimizing End-to-End At-Scale Neural Recommendation
Inference

**Publication:**

ISCA’20

**Problem to solve:**

Optimizing heterogeneous use cases requires tools and flexible systems

1.  Use case diversity: different usage of Recommendation system

2.  Rapid model evolution: different NN models

3.  Hardware heterogeneous: GPU, CPU, ASIC…

**Major contribution:**

This work optimizes recommendation inference perf across heterogeneous hardware,
so this work needs to:

1.  Understand different design space (models, hardware…)

    -   Diversity models: embedding-dominated, MLP-dominated, attention-
        dominated

    -   Different batch sizes affect performance, choose the optimal batchsize
        (query per second: QPS)

    -   Different hardware is suitable for different batch sizes. GPU is
        suitable for large queries and can effectively accelerate the execution
        time of large queries.

2.  Infrastructure to quantify impact of models, hardware

So how to determine CPU and GPU workload is a question. The paper trades off
processing queries on CPUs versus GPUs requires careful optimization. This can
be accomplished by tuning the query-size threshold. Queries larger than this
threshold are offloaded to the GPU while smaller ones are processed on CPU
cores.

The optimal threshold varies across the three recommendation models. In fact,
they find that the threshold not only varies across model architectures, but
also across tail latency targets.

1.  Maximize QPS by balancing data and thread-level parallism

This paper explores how many cores are needed for recommendation, and we can
find that different models need different papalism.

**Lessons learnt:**

1.  Recommendation system applies different models, and each has unique
    requirement for memory bandwidth and performance, so this paper explores the
    characteristic of each model, and chose the optimal hardware to execute each
    model.

2.  This paper discusses the batch parallelism. Compute intensive models are
    typically optimized with lower batch-sizes as compared to memory intensive
    models. This is a result of the compute intensive models being accelerated
    by the data-parallel SIMD units. Thus, throughput for compute intensive
    models is maximized by fully utilizing the data parallel SIMD units. While
    higher throughput is achieved at smaller batchsizes for compute intensive
    models, memory intensive models require larger batch sizes. This is because
    the primary performance bottleneck of models with heavy embedding table
    accesses lies in the DRAM bandwidth utilization. In order to fully utilize
    the memory bandwidth, memory intensive recommendation models must be run
    with higher batch-sizes.

3.  For different hardware, this paper tests Intel Broadwell and Intel Skylake,
    and finds that the optimal batch size is strictly higher on Intel Broadwell
    compared to Skylake. This is a result of the varying cache hierarchies on
    the two platforms. In particular, Intel Broadwell implements an inclusive
    L2/L3 cache hierarchy while Intel Skylake implements an exclusive L2/L3
    cache hierarchy. As a result, Intel Broadwell suffers from higher cache
    contention with more active cores leading to performance degradation.
