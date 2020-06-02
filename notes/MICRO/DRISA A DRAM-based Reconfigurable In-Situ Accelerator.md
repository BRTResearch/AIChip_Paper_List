**Paper title:**

DRISA: A DRAM-based Reconfigurable In-Situ Accelerator

**Publication:**

MICRO’17

**Problem to solve:**

This paper focused on the “memory wall” problem by proposing a
processing-in-memory DRAM architecture.

**Major contribution:**

1.  An accelerator architecture provides large on-chip memory and in-situ
    computing benefits;

2.  A set of circuits and microarchitectures are implemented in DRISA, including
    the BL logic design, the reconfigurable scheme, hierarchical internal data
    movement circuits, and controllers;

3.  Comparison with state-of-the-art ASIC and GPU solutions in CNN acceleration
    cases.

**Lessons learnt:**

This paper uses high-density DRAM technology to create high-performance
accelerators. In order to overcome the problem of too much area and power
consumption cost of complex computing units under DRAM technology, this paper
only designs simple Boolean logic and shift circuits, and uses these circuits in
serial iteration to calculate complex operations such as addition and
multiplication. At the same time, because it is located in the accelerator
design rather than the computable system memory, the design takes performance
optimization as the first goal, effectively sacrificing some area cost in
exchange for higher computing performance.

Overall, this structure shortens the distance between calculation and storage,
reducing the energy consumption of data movement. And this structure makes full
use of a large amount of parallel logic and higher internal bandwidth in DRAM,
and realizes the acceleration of the example application of single-bit weight
neural network.
