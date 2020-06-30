**Paper title:**

Morph: Flexible Acceleration for 3D CNN-based Video Understanding

**Publication:**

MICRO’18

**Problem to solve:**

-   3D CNN consumes lot of energy and computation, and needs to be accelerate

-   Given that 3D CNNs are a generalization of 2D CNNs, a 2D CNN accelerator
    (e.g., Eyeriss [8]) cannot efficiently evaluate a 3D CNN

-   3D CNN memory footprint for both data types far exceeds the typical on-chip
    memory

-   In 3D CNN, input and filter memory requirements vary significantly across
    layers in the case of 3D CNNs. Yet, 2D CNN hardware resources are typically
    provisioned for the worst case layer

-   The number of computations done per Byte of data—is higher for 3D CNNs. This
    not only makes 3D CNNs significantly more compute bound, but also reduces
    the ratio of energy spent accessing the off-chip memory vs. overall energy
    compared to 2D CNNs.

**Major contribution:**

This paper designs and implements Morph: a flexible 3D CNN hardware accelerator.
Morph is the first ASIC accelerator targeting 3D CNNs

-   Buffer hierarchy: A key pre-requisite to exploit data reuse is to design a
    deep enough on-chip buffer hierarchy to support all degrees of temporal
    locality in the data access pattern. In this experiment, for each buffer
    hierarchy, they sweep possible loop orders and tile sizes, fixing the
    physical buffer size to the tile size, to isolate the effect of levels of
    hierarchy.

-   Configurable Buffers: The goal of providing buffer configurability is to
    allow different tile sizes of inputs, filters and psums at each level of the
    buffer hierarchy, while minimizing internal fragmentation in each physical
    buffer. This design is reused for each level of on-chip memory, and is used
    to share space between inputs, filters and psums within a level. Each buffer
    is first divided into Bi banks. Each bank supports a single read and single
    write port.

-   This paper codesigns a software framework that finds proper
    configuration-time parameters (tile sizes, loop order, loop parallelism) for
    each layer of each 3D CNN that runs on the Morph accelerator

-   The optimizer first enumerates all possible configurations. Chosen L2 tile
    sizes serve as a starting point for later heuristics that select sub-tile
    sizes for remaining buffer levels. To reduce search time, the L2 tile size
    and degree of PE parallelism search space can be discretized. The optimizer
    takes the cartesian product of the parameter list to enumerate the
    configurations, where each configuration is [outer loop order, inner loop
    order, Ht, Wt, Ct, Kt, Ft, Hp, Wp, Kp].

-   Based on the current configuration, this step generates metadata required
    for further calculations. This includes: the number of iterations the chosen
    tile has to perform to complete the convolution, storage requirements for
    each of the tiles, overlapped regions for tile slides (halos [12]), the
    final output size, etc.

-   In this step, the optimizer uses a heuristic to set the tile size for each
    data type (inputs, weights, psums) for each level of on-chip memory below
    the last level, given each starting configuration.
