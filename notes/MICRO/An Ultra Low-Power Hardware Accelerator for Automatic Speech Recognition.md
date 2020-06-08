**Paper title:**

An Ultra Low-Power Hardware Accelerator for Automatic Speech Recognition

**Publication:**

MICRO’16

**Problem to solve:**

1.  Viterbi search in ASR (Automatic Speech Recognition) takes dominant part on
    time consumption.

2.  Using GPU to speed up this process needs high energy consumption.

As a result, in mobile devices, an accelerator for Viterbi search is required.

**Major contribution:**

1.  An accelerator for the Viterbi search that achieves 1.7x speedup over a
    high-end desktop GPU (980), while consuming 287x less energy.

2.  A prefetching architecture tailored to the characteristics of the Viterbi
    search algorithm that provides 1.87x speedup over the base design.

3.  A memory bandwidth saving technique that removes 20% of the accesses to
    off-chip system memory.

**Lessons learnt:**

This paper focus on only one algorithm in speech recognition, which is important
and useful. The author finds out the bottleneck of the algorithm is the memory
load part, and this leads to the whole accelerator design.
