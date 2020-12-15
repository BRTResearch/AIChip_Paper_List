**Paper title:**

Newton: A DRAM-maker’s Accelerator-in-Memory (AiM) Architecture for Machine
Learning

**Publication:**

MICRO’2020

**Problem to solve:**

1.  Memory-bound models in machine learning require unprecedented high-bandwidth
    connection between compute and memory.

2.  Previous PIM (processing-in memory) and PNM (processing-near memory)
    approaches advocate full processor cores which do not conform to PIM’s
    severe area and power constraints.

3.  For digital PIM, compute area and power are constrained to avoid excessive
    DRAM density loss and thermal challenges.

**Major contributions:**

1.  Proposed Newton, which places a minimal compute of only multiply-accumulate
    units and buffers in the DRAM which avoids the full-core area and power
    overheads of previous work.

2.  Employed a DRAM-like interface for the host to issue commands to the PIM
    compute.

3.  Introduced optimizations to prevent the PIM-host interface from becoming a
    bottleneck.

4.  Employed an unusually wide interleaved layout for the matrix to capture
    output vector reuse with reasonable buffering.
