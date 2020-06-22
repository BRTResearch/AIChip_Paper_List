**Paper title:**

Enabling Highly Efficient Capsule Networks Processing Through A PIM-Based
Architecture Design

**Publication:**

HPCA’20

**Problem to solve:**

CapsNets exhibit low efficiency due to the special program and execution
features of their routing procedure, including massive unsharable intermediate
variables and intensive synchronizations, which are very difficult to optimize
at software level.

**Major contribution:**

1.  Execution inefficiency analysis: They conduct a comprehensive
    characterization study on CapsNet inference on modern GPUs and identify its
    root causes for execution inefficiency.

2.  Processing-in-memory based hybrid computing architecture: we propose a
    processing-in-memory based hybrid computing architecture named PIM-CapsNet,
    which leverages both GPU on-chip computing capability and off-chip in-memory
    acceleration features of 3D stacked memory to improve the overall CapsNet
    inference performance.

3.  Memory-level optimization: Several memory-level optimizations were proposed
    to enable minimal in-memory communication, maximum parallelization, and low
    design complexity and overhead

**Lessons learnt:**

This paper proposes a hybrid computing architecture design named PIM-CapsNet. It
preserves GPU’s on-chip computing capability for accelerating CNN types of
layers in CapsNet, while pipelining with an off-chip in-memory acceleration
solution that effectively tackles routing procedure’s inefficiency by leveraging
the processing-in-memory capability of today’s 3D stacked memory. Using routing
procedure’s inherent parallellization feature, the design enables hierarchical
improvements on CapsNet inference efficiency through minimizing data movement
and maximizing parallel processing in memory.
