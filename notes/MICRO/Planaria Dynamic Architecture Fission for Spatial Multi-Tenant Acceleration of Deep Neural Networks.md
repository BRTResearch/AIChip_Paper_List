**Paper title:**

Planaria Dynamic Architecture Fission for Spatial Multi-Tenant Acceleration of
Deep Neural Networks

**Publication:**

MACRO’20

**Problem to solve:**

1.  Experience in cloud accelerator systems shows that keeping multiple models
    simultaneously resident on an accelerator has deployment benefits. Yet, only
    this year PREMA has explored a scheduling algorithm that time-multiplexes a
    DNN accelerator across different DNNs through preemption.

2.  How to run multiple models simultaneously in the neural network accelerator.

**Major contribution:**

1.  This paper introduces and explores the dimension of dynamic fission in DNN
    accelerators. This innovation enables simultaneous execution of multiple DNN
    acceleration threads to be spatially co-located on the same hardware
    substrate.

2.  The paper devises a concrete microarchitecture as an instance of dynamic
    fissionable architectures by delving into the design challenges associated
    with offering this technology on TPU-like systolic designs.

3.  To leverage architecture-level fission, the paper defines a task scheduling
    algorithm that breaks up the accelerator with respect to the current server
    load, DNN topology, and task priorities, all while considering the latency
    bounds of the tasks.

**Lessons learnt:**

This paper use a set of multiplexers around a PE which can enable
omni-directional movement, so that the omni-directional systolic array can
enable richer fission and rearrangement possibilities.
