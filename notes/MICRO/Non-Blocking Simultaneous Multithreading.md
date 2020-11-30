**Paper title:**

Non-Blocking Simultaneous Multithreading: Embracing the Resiliency of Deep
Neural Networks

**Publication:**

MICRO’20

**Problem to solve:**

DNNs exhibit inefficiencies when considering the actual values that propagate
through the layers, which cause spontaneous underutilization of the MAC units.

**Major contribution:**

1.  Introduce the concept of non-blocking simultaneous multithreading (NB-SMT),
    which increases DNN hardware utilization by exploiting DNN algorithmic
    resiliency and unstructured sparsity.

2.  Exploit DNNs’ resiliency and temporarily reducing the threads’ numerical
    precision so that execution units are still able to accommodate all thread
    computations in that same cycle.

3.  Reorder the matrices according to per-layer statistics which are gathered
    once on the activations, to reduce the number of value rounding.

**Lessons learnt:**

1.  A flexible multiplier units capable of conducting different precision
    multiplications on demand.

2.  An approach that use two 4-8 multiplier, to run two 8bit\*8bit
    multiplication, with reduction of precision.
