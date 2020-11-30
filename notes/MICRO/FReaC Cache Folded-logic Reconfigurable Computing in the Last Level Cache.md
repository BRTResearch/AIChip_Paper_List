**Paper title:**

FReaC Cache: Folded-logic Reconfigurable Computing in the Last Level Cache

**Publication:**

MICRO’20

**Problem to solve:**

1.  The need for high energy efficiency results in the growing of custom and
    reconfigurable accelerators. Existing solutions suffer from the high latency
    and energy cost of data transfers. There is a need to design a fast,
    energy-efficient and programmable reconfigurable computing architecture.

2.  Solutions of NMA (near memory accelerators) and PIM (processing in memory)
    require changes to the host processor and add custom instructions in ISA.

3.  Most of accelerators are domain specific which fail to be modified easily to
    adapt to new algorithms.

**Major contributions:**

1.  Proposed FReaC Cache, which only changes the last level cache and avoid
    addition of custom instructions.

2.  Proposed a novel architecture in LLC, including dense compute subarrays,
    micro compute clusters (MCC).

3.  Proposed architectures for subarray, MCC, and explained the setup and
    configuration.

4.  Introduced logic folding and algorithm to map the accelerators on the
    architecture.

**Lessons learnt:**

This paper exploits the architecture for accelerators with performance
improvements and small overhead in area. The architecture doesn’t change the
existing subarray in LLC but add new circuits and doesn’t require custom
instructions. Compared to FPGA, it’s more area and power efficient, which is
attractive for this paper.
