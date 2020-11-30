**Paper title:**

In-Datacenter Performance Analysis of a Tensor Processing Unit

**Publication:**

ISCA’2017

**Problem to solve:**

This paper describes and measures the Tensor Processing Unit (TPU) and compares
its performance and power for inference to its contemporary CPUs and GPUs.

**Major contribution:**

1.  The TPU leverages the order-of-magnitude reduction in energy and area of
    8-bit integer systolic matrix multipliers over 32-bit floating-point
    datapaths of a K80 GPU to pack 25 times as many MACs (65,536 8-bit vs. 2,496
    32-bit) and 3.5 times the on-chip memory (28 MiB vs. 8 MiB) while using less
    than half the power of the K80 in a relatively small die. This larger memory
    helps increase the operational intensity of applications to let them utilize
    the abundant MACs even more fully.

2.  We found that despite a recent emphasis on CNNs in the architecture
    community, they constitute only about 5% of the representative NN workload
    for our datacenters, which suggests more attention should be paid to MLPs
    and LSTMs. Repeating history, it’s similar to when many architects
    concentrated on floating-point performance when most mainstream workloads
    turned out to be dominated by integer operations. We observed that
    inferences per second (IPS) is more a function of the NN than of the
    underlying hardware, and so IPS is an even worse single performance metric
    for NN processors than MIPS and MFLOPS are for CPUs and GPUs.

3.  We also learned that inference applications have serious response-time
    bounds because they are often part of user facing applications, thus NN
    architectures need to perform well when coping with 99th-percentile latency
    deadlines. While the K80 may excel at training, on average it is just a
    little faster than Haswell at inference for our workload, perhaps because of
    its emphasis on throughput rather than latency; that conflicts with the
    strict response-time deadlines of our inference applications. The TPU die
    leverages its advantage in MACs and on-chip memory to run short programs
    written using the domain-specific TensorFlow framework 15 times as fast as
    the K80 GPU die, resulting in a performance per Watt advantage of 29 times,
    which is correlated with performance per total cost of ownership. Compared
    to the Haswell CPU die, the corresponding ratios are 29 and 83. While future
    CPUs and GPUs will surely run inference faster, a redesigned TPU using circa
    2015 GPU memory would go two to three times as fast and boost the
    performance/Watt advantage to nearly 70 over the K80 and 200 over Haswell.

**Lessons learnt:**

The TPU succeeded because of the large—but not too large—matrix multiply unit;
the substantial software-controlled on-chip memory; the ability to run whole
inference models to reduce dependence on its host CPU; a single-threaded,
deterministic execution model that proved to be a good match to 99th-percentile
response time limits; enough flexibility to match the NNs of 2017 as well as of
2013; the omission of general purpose features that enabled a small and low
power die despite the larger datapath and memory; the use of 8-bit integers by
the quantized applications; and that applications were written using TensorFlow,
which made it easy to port them to the TPU at high performance rather than them
having to be rewritten to run well on the very different TPU hardware.
Order-of-magnitude differences between products are rare in computer
architecture, which may lead to the TPU becoming an archetype for
domain-specific architectures. We expect that many will build successors that
will raise the bar even higher.
