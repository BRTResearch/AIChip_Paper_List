**Paper title:**

DeftNN: Addressing Bottlenecks for DNN Execution on GPUs via Synapse Vector
Elimination and Near-compute Data Fission

**Publication:**

MICRO’17

**Problem to solve:**

The state-of-the-art techniques to improve DNN performance have significant
limitations in bridging the gap on real systems. Current network pruning
techniques remove computation, but the resulting networks map poorly to GPU
architectures, yielding no performance benefit or even slowdowns. Meanwhile,
current bandwidth optimization techniques focus on reducing off-chip bandwidth
while overlooking on-chip bandwidth, a key DNN bottleneck.

The paper aims to speed up the DNN on GPU by solving the GPU-suitable network
pruning and on-chip bandwidth optimization problems.

**Major contribution:**

This paper describes DeftNN, a system for optimizing GPU-based DNNs. DeftNN uses
two novel optimization techniques: synapse vector elimination, a technique that
drops the non-contributing synapses in the neural network, as well as
near-compute data fission, a mechanism for scaling down the data movement
requirements within DNN computations. The proposed experimental results show
that DeftNN can significantly improve DNN performance, improving performance by
over 2.1x on commodity GPU hardware and over 2.6x when leveraging a small
additional hardware unit that accelerates fission.

The main contribution is as follow:

1.  Introducing a DNN optimization technique for GPUs, synapse vector
    elimination, that shrinks the topology of the neural network. This method is
    guided by the insight that network pruning techniques in DNN systems must
    have computational regularity to achieve significant speedups. Experiments
    show that synapse vector elimination achieves 1.5x average end-to-end
    speedups on a set of 6 state-of-the-art DNNs on real GPU hardware.

2.  Introducing near-compute data fission, which improves performance by
    efficiently packing on-chip memory. To realize speedup, the authors argue
    that the focus must be shifted from minimizing data size to minimizing
    unpacking overhead. The near-compute data fission provides 1.6x end-to-end
    speedup on a set of 6 DNNs on real GPU hardware available today by
    performing unpacking in software. A lightweight hardware extension (\<0.25%
    area overhead) to facilitate efficient unpacking is also introduced,
    achieving an additional 1.4x speedup over software-only near-compute data
    fission.

3.  Introducing DeftNN, a state-of-the-art GPU DNN execution framework which
    automatically applies synapse vector elimination and near-compute data
    fission optimizations to existing DNN software applications to dramatically
    improve performance on today’s GPUs. DeftNN is evaluated on real GPU
    hardware across 6 state-of-the-art DNNs, covering both fully connected and
    convolutional layers, showing significant performance improvements as 2.1x
    speedups on average.

**Lessons learnt:**

The paper focused on GPU accelerating, and mainly discussed the matrix
multiplication operations. The on-chip data compression is a very inspiring
idea, making use of idle function unit cycles.
