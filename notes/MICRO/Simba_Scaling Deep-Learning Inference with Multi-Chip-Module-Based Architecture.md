**Paper title:**

Simba: Scaling Deep-Learning Inference with Multi-Chip-Module-Based Architecture

**Publication:**

MICRO’19

**Problem to solve:**

Package-level integration using multi-chip-modules (MCMs) is a promising
approach for building large-scale systems. Compared to a large monolithic die,
an MCM combines many smaller chiplets into a larger system, substantially
reducing fabrication and design costs. While MCMs have been used for general
compute systems, applying MCMs to high-performance DNN inference algorithms has
not been previously examined. Specific challenges stem from the natural
non-uniformity between on-chip and on-package bandwidth and latency. While
multi-chip systems also exhibit similar forms of non-uniformity, this paper
focuses on the specific characteristics of MCM-based systems as they provide a
natural progression from monolithic single-chip inference accelerators as
semiconductor scaling slows.

**Major contribution:**

This paper presents Simba, a scalable deep-learning inference accelerator
employing multi-chip-module-based integration and proposes three
tail-latency-aware, non-uniform tiling optimizations targeted at improving
locality and minimizing inter-chiplet communication: (1) non-uniform work
partitioning to balance compute latency with communication latency; (2)
communication-aware data placement to minimize inter-chiplet traffic; and (3)
cross-layer pipelining to improve resource utilization.

**Lessons learnt:**

The optimizations of this paper achieve up to 16% speedup compared to the
baseline layer mapping. The evaluation shows that Simba can process 1988
images/s running ResNet-50 with batch size of one, delivering inference latency
of 0.50 ms.
