**Paper title:**

A Multi-Neural Network Acceleration Architecture

**Publication:**

ISCA’20

**Problem to solve:**

Existing accelerators which are optimized for a single neural network execution
can suffer from severe resource underutilization when running multiple neural
networks, mainly due to the load imbalance between computation and memory-access
tasks from different neural networks.

**Major contribution:**

1.  **Multi-Neural Network Acceleration Architecture**: To the best of
    knowledge, this is the first work to propose an accelerator architecture to
    enable a cost-effective multi-neural network execution.

2.  **Hardware-based Scheduling**: AI-MT exploits three hardware-based
    scheduling methods to efficiently schedule dependency-free sub-layer tasks:
    memory block prefetching and compute block merging for the best resource
    load matching, and memory block eviction for the minimum on-chip memory
    footprint.

3.  **Minimum SRAM Requirement**: AI-MT significantly reduces its on-chip SRAM
    capacity requirement, which is a critical contribution for future
    scalability.

**Lessons learnt:**

The discussion in this article is very similar to the idea discussed before,
that is, cloud servers provide efficient neural network calculations with
different network structures. The key idea of AI-MT is to fully utilize the
accelerator’s computation resources and memory bandwidth by creating fine-grain
computation and memory-access tasks from different networks, scheduling the best
load matching tasks during runtime, and executing them in parallel.

During compile time, AI-MT divides each layer into multiple identical sub-layers
to create fine-grain computation and memory-access tasks. Then, AI-MT generates
the sub-layer scheduling table to keep the sub-layer level metadata required to
the fine-grain task management at runtime. AI-MT can naturally divide each layer
into sub-layers at compile time without sacrificing performance.

During runtime, AI-MT dynamically schedules fine-grain computation and
memory-access tasks from multiple networks. AIMT tracks the dependency-free MBs
and CBs by referring to the sub-layer scheduling tables, and then applies load
balancing scheduling mechanism. The load balancing scheduling mechanism fetches
dependency-free MBs early to fully utilize the accelerator’s memory bandwidth
resources, and groups dependency-free CBs to fully utilize the computing
resources available. On top of the load balancing scheduling mechanism, AI-MT
applies early MB eviction, which can early schedule and evict SRAM
capacity-critical MBs to minimize the on-chip memory’s capacity requirement.
