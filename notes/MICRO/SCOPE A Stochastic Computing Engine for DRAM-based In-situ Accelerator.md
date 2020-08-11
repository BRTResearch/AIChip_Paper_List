**Paper title:**

SCOPE: A Stochastic Computing Engine for DRAM-based In-situ Accelerator

**Publication:**

MICRO’18

**Problem to solve:**

It redesigns both the compute and memory and put them as close together as
possible to embrace local memory’s latency/bandwidth benefits and to reduce data
movement overhead. First, one is the memory-rich processor, which packs as much
memory as possible with the conventional processor or accelerators. However, duo
to the large SRAM/eDRAM cell, the memory capacity is limited, thus the data
movement overhead still remains a problem. The performance of such
interposer-connected dense memory is not competitive with on chip local memory.
Second is compute-capable memory, which is also known as processing in memory
(PIM). However, system memory is highly optimized for low cost, and therefore
the processing unit added to the memory has tight area and power constraints.
Third, due to the inefficiency of building processing logic circuits with the
DRAM technology, it only supports simple bitwise operations (NOR) and bitwise
shifts. To support complex computation such as addition, it breaks those
instructions in multiple bitwise Boolean logic operations and processes them one
by one, which take hundreds of cycles.

**Major contribution:**

1.  It proposes the idea of applying stochastic computing to the DRAM-based
    in-situ accelerator architecture to synergistically reinforce the strengths
    and address the weaknesses of both paragigms.

2.  It demonstrates SCOPE, the holistic architecture design thet supports
    stochastic computing in the in-situ accelerator.

3.  It proposes a novel Hierarchical and Hybrid Deterministic(H2D) stochastic
    computing arithmetic, providing better performance, lower area overhead, and
    better numerical precision.

**Lessons learnt:**

This paper mainly aims at realizing stochastic computation in DRAM, and proposes
H2D algorithm to improve this process.
