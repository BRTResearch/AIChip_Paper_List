**Paper title:**

Wire-Aware Architecture and Dataflow for CNN Accelerators

**Publication:**

MICRO’19

**Problem to solve:**

In spite of several recent advancements, data movement in modern CNN
accelerators remains a significant bottleneck. Several data movements in prior
works such as Eyeriss and TPU v1 architectures are across long wires, and
account for much of the energy consumption. In this paper, we re-visit the
design of PEs and memory hierarchy for CNN accelerators, with a focus on
reducing these long and frequently traversed wire lengths.

**Major contribution:**

To tackle the above problems, the paper mainly makes the contributions as
follows:

1.  It creates a new wire aware accelerator WAX, which implements a deep and
    distributed memory hierarchy to support short wires. WAX implement an array
    of PEs beside each cache subarray. Each PE is assigned less than a handful
    of registers. The registers have shift capabilities to implement an
    efficient version of systolic dataflow. Each PE therefore uses minimal
    wiring to access its few registers, its adjacent register, and a small
    (few-KB) cache subarray. Data movement within this basic WAX tile has thus
    been kept to a minimum.

2.  It introduces a novel family of dataflows that perform a large slice of
    computation with high reuse and data movement largely confined within a
    tile, which increases the computational power of the WAX tile. The authors
    explore how the dataflows can be adapted to reduce problematic partial sum
    updates in the subarray.

**Lessons learnt:**

Since WAX can perform calculations while loading sub-arrays, it has a higher
calculation utilization rate, which is 2 times higher than the performance of
Eyeriss. In terms of energy, WAX yields 2.6-4.4× improvement, relative to
Eyeriss. By removing a large number of register files in each PE in Eyeriss, the
overall chip area is reduced, and therefore the clock distribution power is also
reduced.
