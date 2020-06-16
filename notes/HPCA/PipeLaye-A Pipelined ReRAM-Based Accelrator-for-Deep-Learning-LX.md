**Paper title:**

PipeLayer: A Pipelined ReRAM-Based Accelerator for Deep Learning

**Publication:**

HPCA’17

**Problem to solve:**

ReRAM can be employed to perform neural computations in memory, while training
cannot be efficiently supported with the current existing schemes. First, they
do not consider weight update and complex data dependency in training procedure.
Second, deep pipeline designed in current accelerator is only beneficial when a
large number of consecutive images can be fed into the architecture. Third, the
deep pipeline is vulnerable to pipeline bubbles and execution stall. If there is
an accelerator for both training and testing, that would be great.

**Major contribution:**

1.  This paper proposed PipeLayer, a ReRAM-based PIM accelerator for CNNs that
    CNNs that for the first time support both training and testing. It proposed
    efficient pipeline to exploit intra- and inter-layer parallelism. PipeLayer
    enables the highly pipelined execution of both training and testing, without
    introducing the potential stalls in previous work.

2.  This paper evaluated the accelerator and demonstrated achieving the speedups
    of 42.45x compared with GPU platform on average. The average energy saving
    compared with GPU implementation is 7.17x.

**Lessons learnt:**

1.  New techniques can bring some revolutions for architecture, like 3D-stacking
    technology, PIM or near data computing. Decoupling logic and memories with a
    logic layer that encapsulates processing units to perform computation.

2.  Incorporating the pipeline mechanism into ReRAM-based architecture would be
    effective in domain specific optimization.
